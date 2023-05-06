# Apps Bunches Recommendation For Zid Themes Developers

## The following tips are the best way to make your theme compatible with apps bunches mobile app

## Slider Module
* The supported file names : ```main-slider.twig``` , ```main_slider2.twig``` , ```slider.twig``` , ```sslider.twig``` , ```img-slider.twig``` , ```templete-velvet-main-slider.twig```
* The supported slider items list key is ```slider```store-description.twig
* The supported slider items hide dots key is ```hide_dots``` it should be boolean if null we will consider it as true
* The supported slider item type key is ```type``` it must be ```video``` or ```image``` if null we will consider it an image
* The supported slider item image keys are ```mobile_image``` , ```image_mobile``` , ```image```
* The supported slider item vedio keys are ```url``` , ```link```
* The supported slider item title key is ```title```
* The supported slider item sub title keys are ```subtitle``` , ```des```
* The supported slider item button title key is ```btn_text```
* The supported slider item text color key is ```text_color``` if null we will use white color
* The supported slider item buttom background color key is ```background_color``` if null we will use primary color
* The supported slider item link key are ```url``` , ```link```

## Gallery Module
* The supported file names : ```gallery.twig``` , ```ggallery.twig``` , ```template-velvet-gallery.twig``` , ```home-banners-section.twig```
* The supported gallery items list keys are ```gallery``` , ```ads```
* The supported gallery main title key is ```title```
* The supported gallery item image key is ```image```
* The supported gallery item link keys are ```url``` , ```link```
* The supported gallery item title key is ```title```
* The supported gallery item sub title keys are ```subtitle``` , ```des```
* The supported gallery item button visibility key is ```show_button``` it should be boolean if null we will consider it as true
* The supported gallery item show button with border key is ```full_btn_border``` it should be boolean if null we will consider it as false
* The supported gallery item button title keys are ```btn_text``` , ```button_text``` , ```buttonText```
* The supported gallery item text color key is ```text_color``` if null we will use white color
* The supported gallery item buttom background color key is ```button_color``` if null we will use primary color

## Feature Module
* The supported file names : ```features.twig``` , ```store-features.twig``` , ```features-section.twig```
* The supported feature items list keys are ```features``` , ```store_features```
* The supported feature items background color key is ```bg_color``` if null we will use white color
* The supported feature item image key is ```image``` it must be not null
* The supported feature item title keys are ```title``` , ```text```
* The supported feature item description keys are ```des``` , ```desc```
* The supported feature item text color key is ```text_color``` if null we will use black color

## Products Module
* The supported file names : ```products.twig``` , ```offers.twig``` , ```products-section.twig``` , ```features-section.twig``` , ```product_grid.twig``` ,```top_picks_products.twig``` , ```bestseller-section.twig``` , ```products-selected.twig``` , ```home-featured-products-section.twig```
* The supported products moudule keys are ```products``` , ```last_products```
* The supported products in the moudule key is ```products```
* The supported products title key is ```name```
* The supported products display key is ```display``` it must be boolean if null we will consider it as true
* The supported products url key is ```url```
* The supported products module type key is ```module_type```
* The supported products id key is ```id``` it may used if the products related with one category
* The supported products more button object key is ```more_button``` and contains the ```text``` and ```url```

## Category Module
* The supported file names : ```category-products-section.twig``` , ```home-category-products.twig``` , ```home-products-section.twig```
* The supported catgory moudule key is ```category```
* The supported category id key is ```id``` it used for moving to category page
* The supported category name key is ```name```
* The supported products in the moudule key is ```products```
* The supported category display more button key is ```display_more``` it must be boolean if null we will consider it as true


## Categories Module
* The supported file names : ```category-section.twig``` , ```template-velvet-category-section.twig``` , ```home-categories.twig``` , ```categories.twig``` , ```categories_banner.twig``` , ```categories-selected.twig``` , ```home-categories-section.twig```
* The supported main title keys are ```title``` , ```sectionTitle```
* The supported sub title key is ```sectionSubTitle```
* The supported categories display more button key is ```display_more``` it must be boolean if null we will consider it as false
* The supported more text button key is ```more_text```
* The supported cateogries items keys are ```categories``` , ```category_items``` but in the last one the category object must be named with ```item``` 


## Categories with Products Module
* The supported file names : ```product-category.twig``` 
* The supported moudule key is ```products``` and must contains a category object named ```category``` and contains products with list named ```products```
* The supported main title key is ```title```
* The supported categories display more button key is ```display_more``` it must be boolean if null we will consider it as false


## Instagram Moudule
* The supported file names : ```instagram-gallery.twig``` 
* The supported main title key is ```title```
* The supported instagram username account key is ```instagram_account```
* The supported images list key is ```instagram``` and every object must contains ```image``` and ```url```

## Banner Moudule
* The supported file names : ```banner.twig``` , ```large-banner.twig``` , ```big-banner.twig```
* The supported banner image keys are ```mobile_image``` , ```image_mobile``` , ```image```
* The supported banner link keys are ```url``` , ```link```
* The supported banner background color key is ```color``` if null we will use white color
* The supported banner title key is ```title```
* The supported banner sub title keys are ```subtitle``` , ```des``` , ```desc```
* The supported banner title text color key is ```text_color``` if null we will use white color
* The supported banner button visibility key is ```show_button``` it should be boolean if null we will consider it as true
* The supported banner button title keys are ```button_text``` , ```button```
* The supported banner button text color key is ```button_text_color``` if null we will use white color
* The supported banner button background color key is ```button_bg_color``` if null we will use primary color

## Brand Moudule
* The supported file names : ```home-brands-section.twig``` , ```home-brands.twig```
* The supported brand list key is ```brands```
* The supported brand list title key is ```title```
* The supported brand item image key is ```image```
* The supported brand item url keys are ```url``` , ```link```

## Description Moudule 
* The supported file names : ```store-description.twig```
* The supported store title key is ```title```
* The supported store description keys are ```des``` , ```desc``` 
* The supported social media visibility key is ```display_social_media```
* The suppotted titkok link key must be as ```tiktok``` in ```items``` in ```social_media``` in ```footer```
* The suppotted twitter link key must be as ```twitter``` in ```items``` in ```social_media``` in ```footer```
* The suppotted instagram link key must be as ```instagram``` in ```items``` in ```social_media``` in ```footer```
* The suppotted facebook link key must be as ```facebook``` in ```items``` in ```social_media``` in ```footer```
* The suppotted snapchat link key must be as ```snapchat``` in ```items``` in ```social_media``` in ```footer```

## FAQs Moudule
* The supported file names : ```home-faqs-section.twig```
* The supported FAQs list key is ```faqs_store_features``` and every object should contains ```title``` and ```answer```
* The supported FAQs background color key is ```details_bg``` if null we will use white color
* The supported FAQs video image key is ```details_video_img```
* The supported FAQs video url key is ```details_video``` should be a youtube video url
* The supported FAQs title key is ```details_title```
* The supported FAQs description key is ```details_desc```

## Testimonials Moudule
* The supported file names : ```testimonials.twig``` , ```home-reviews-section.twig``` , ```home-testimonials-section.twig```
* The supported testimonials list keys are ```testimonials``` , ```testimonial``` , ```reviews```
* The supported main title keys are ```title``` , ```title_offer``` , ```sectionTitle```
* The supported testimonial item title keys are ```name``` , ```client_name``` , ```customer_name``` , ```customerName```
* The supported testimonial item date key is ```date```
* The supported testimonial item title keys are ```text``` , ```reviews``` , ```client_opinion``` , ```content``` , ```customerReview```

## Partners Moudule
* The supported file names : ```partners.twig```
* The supported partners list key is ```store_partners```
* The supported main title key is ```title```
* The supported partner item image key is ```image```
* The supported partner url image keys are ```url``` , ```link```

## Video Moudule
* The supported file names : ```video.twig```
* The supported video url key is ```video```
* The supported control buttons visibility key is ```controls```
* The supported auto play key is ```autoplay``` it should be boolean if null we will consider it as false
* The supported main title key is ```title```

## Countdown Moudule
* The supported file names : ```countdown_banner.twig```
* The supported countdown date key is ```countdownDate```
* The supported countdown banner key is ```countdownImage``` it should be a list of object named ```image```

