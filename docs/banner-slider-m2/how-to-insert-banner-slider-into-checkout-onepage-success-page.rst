How to insert Banner slider into checkout onepage success
=========================================================

In this guide, we will show you how to insert a banner slider into checkout onepage success

Create a new file call `checkout_onepage_success.xml` in `app/code/Mageplaza/BetterSlider/view/frontend/layout/` . Full path is `app/code/Mageplaza/BetterSlider/view/frontend/layout/checkout_onepage_success.xml`.
You also can paste the following code into your theme layout.
    .. note::
        - You also can create the xml file in theme folder or copy into an other module.
        - `banner_id` value should be changed to your own.
        - Default path: `app/code/Mageplaza/BetterSlider/view/frontend/layout/`



Begin of Content
-----------------------


Paste the following content into `checkout_onepage_success.xml`::

  <?xml version="1.0"?>
  <page xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:noNamespaceSchemaLocation="../../../../../../../lib/internal/Magento/Framework/View/Layout/etc/page_configuration.xsd">
    <body>
        <referenceContainer name="content">
            <block class="Mageplaza\BetterSlider\Block\Slider" template="Mageplaza_BetterSlider::slider.phtml"
                   name="bannerslider.checkout.content.top" before="-">
                <action method="setPosition">
                    <argument name="position" xsi:type="string">checkout-content-top</argument>
                </action>
                <action method="setBannerId">
                    <argument name="banner_id" xsi:type="string">2</argument>
                </action>
            </block>
        </referenceContainer>
    </body>
  </page>
  
  
End of Content
-----------------------


Paste the following content into `checkout_onepage_success.xml`::

  <?xml version="1.0"?>
  <page xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:noNamespaceSchemaLocation="../../../../../../../lib/internal/Magento/Framework/View/Layout/etc/page_configuration.xsd">
    <body>
        <referenceContainer name="content">
            <block class="Mageplaza\BetterSlider\Block\Slider" template="Mageplaza_BetterSlider::slider.phtml"
                   name="bannerslider.checkout.content.bottom" before="+">
                <action method="setPosition">
                    <argument name="position" xsi:type="string">checkout-content-bottom</argument>
                </action>
                <action method="setBannerId">
                    <argument name="banner_id" xsi:type="string">2</argument>
                </action>
            </block>
        </referenceContainer>
    </body>
  </page>

  
.. include:: ../ad_footer.rst