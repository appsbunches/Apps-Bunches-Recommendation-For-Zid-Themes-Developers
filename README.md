# Apps Bunches Recommendations for Zid Theme Developers

## Overview
* This document outlines the best practices and supported file structures for integrating Zid themes with the Apps Bunches mobile application. By following these recommendations, developers can ensure optimal compatibility, functionality, and user experience.

## Slider Module
* The supported file names : ```main-slider.twig``` , ```main_slider2.twig``` , ```slider.twig``` , ```sslider.twig``` , ```img-slider.twig``` , ```templete-velvet-main-slider.twig``` , ```slider_img.twig```
* The supported slider items list key is ```slider```store-description.twig
* The supported slider items hide dots key is ```hide_dots``` it should be boolean if null we will consider it as true
* The supported slider item type key is ```type``` , ```slider_type``` it must be ```video``` or ```image``` if null we will consider it an image
* The supported slider item image keys are ```mobile_image``` , ```image_mobile``` , ```image``` , ```img_slider_mobile``` , ```img_slider```
* The supported slider item vedio keys are ```url``` , ```link``` , ```url_button``` , ```video_link```
* The supported slider item title key is ```title```
* The supported slider item sub title keys are ```subtitle``` , ```des```
* The supported slider item button title key is ```btn_text``` , ```text_button```
* The supported slider item text color key is ```text_color``` , ```textColor``` if null we will use white color
* The supported slider item buttom background color key is ```background_color``` if null we will use primary color
* The supported slider item link key are ```url``` , ```link``` , ```url_button``` , ```video_link```

```
{
  "modules": [
    {
      "id": "406b63d8-e1a5-46bb-9a95-089826d78f84",
      "storefront_theme_store_id": "41460ab1-bbbf-4c59-bb06-542575a4e59a",
      "storefront_theme_file_id": "7fe32e1d-f0c3-4c6c-ab5f-d3047494a91b",
      "settings": {
        "slider": [
          {
            "title": "عنوان على الصورة",
            "des": "النص على الصورة",
            "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/ff65a529-b3e4-4f67-9afe-22dad83ed131.png",
            "url": "/products/1-النباتات-الاكسسوارات"
          },
          {
            "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/73c86dc9-0709-46f7-8dce-21b947c0b861.png",
            "url": "/products/عمال-الطاقة-الطبيعي-للنساء"
          },
          {
            "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/0e1bb51b-9310-49e3-958e-24a839a6ac3b.png"
          }
        ],
        "background_color": "#ff6c40",
        "text_color": "#fff5f5",
        "order": 0,
        "hide_dots": false
      },
      "is_draft": 0,
      "draft_for": null,
      "is_deleted": 0,
      "created_at": "2022-04-10T23:33:45.000000Z",
      "updated_at": "2023-05-06T09:25:46.000000Z"
    }
  ]
}

```



## Gallery Module
* The supported file names : ```gallery.twig``` , ```ggallery.twig``` , ```template-velvet-gallery.twig``` , ```home-banners-section.twig```
* The supported gallery items list keys are ```gallery``` , ```ads```
* The supported gallery main title key is ```title``` , ```banner_title```
* The supported gallery item image key is ```image``` , ```img```
* The supported gallery item link keys are ```url``` , ```link``` , ```url_button``` , ```video_link```
* The supported gallery item title key is ```title```
* The supported gallery item sub title keys are ```subtitle``` , ```des``` , ```sub_title```
* The supported gallery item button visibility key is ```show_button``` it should be boolean if null we will consider it as true
* The supported gallery item show button with border key is ```full_btn_border``` it should be boolean if null we will consider it as false
* The supported gallery item button title keys are ```btn_text``` , ```button_text``` , ```buttonText``` , ```text_button```
* The supported gallery item text color key is ```text_color``` , ```textColor``` if null we will use white color
* The supported gallery item buttom background color key is ```button_color``` if null we will use primary color

```
{
  "modules": [
    {
      "id": "205e9d90-acf2-4123-ab70-0678f513d2c2",
      "storefront_theme_store_id": "e63c0adb-5f1d-44cb-9e48-4be4b4065a2a",
      "storefront_theme_file_id": "472f4d3f-944d-4b66-89c1-a5fc300bcaea",
      "settings": {
        "gallery": [
          {
            "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/fd3631ed-0a8e-40c1-a84c-8489a6f221cb.jpg",
            "title": "Abdallah Test Abdallah Test Abdallah Test Abdallah Test Abdallah Test Abdallah Test Abdallah Test ",
            "subtitle": "Test ",
            "text_color": "#ffffff",
            "show_button": true,
            "full_btn_border": true,
            "button_text": "Abdallah Button Abdallah Button Abdallah Button Abdallah Button ",
            "button_color": "#ff0000",
            "url": "/products/عبدالله-تست"
          },
          {
            "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/5470e58d-4964-47be-b8b4-14c5259c1cd3.jpg",
            "title": "Turki",
            "subtitle": "Turki Description",
            "text_color": "#ffffff",
            "show_button": true,
            "full_btn_border": true,
            "button_text": "Turki Button",
            "button_color": "#2500ff",
            "url": "/products/محمود-:-)"
          },
          {
            "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/73ce1bd7-45bf-4c57-b217-73d1599b371e.jpg",
            "title": "Hosam",
            "subtitle": "Test"
          }
        ]
      }
    }
  ]
}

```


## Feature Module
* The supported file names : ```features.twig``` , ```store-features.twig``` , ```features-section.twig```
* The supported feature items list keys are ```features``` , ```store_features```
* The supported feature items background color key is ```bg_color``` if null we will use white color
* The supported feature item image key is ```image``` , ```img``` it must be not null
* The supported feature item title keys are ```title``` , ```text```
* The supported feature item description keys are ```des``` , ```desc```
* The supported feature item text color key is ```text_color``` if null we will use black color

```
{
    "modules": [
        {
            "id": "8392e220-494a-452b-8081-4c{2525eed0e",
            "storefront_theme_store_id": "e63c0adb-5f1d-44cb-9e48-4be4b4065a2a",
            "storefront_theme_file_id": "f8cca0fb-1b0d-45c4-a005-429a192f1793",
            "settings": {
                "features": [
                    {
                        "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/0df62d8f-5204-4d4b-b70b-2e1a5ae4862e.png",
                        "text": "طرق دفع متعددة",
                        "text_color": "#ff0000"
                    },
                    {
                        "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/48688ef9-8e4f-4f03-909f-7b4327b338af.png",
                        "text": "شحن سريع",
                        "text_color": "#5aff89"
                    },
                    {
                        "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/d86edf82-b998-4d66-bf62-346a20505fe8.png",
                        "ضمان بعد الشراء": "text",
                        "text_color": "#f4e32f"
                    }
                ],
                "bg_color": "#481229",
                "order": 11
            },
            "is_draft": 0,
            "draft_for": null,
            "is_deleted": 0,
            "created_at": "2022-05-25T07:57:44. 000000Z",
            "updated_at": "2022-09-03T17:28:46.000000Z",
        }
    ]
}
```


## Products Module
  * The supported file names : ```products.twig``` , ```offers.twig``` , ```products-section.twig``` , ```features-section.twig``` , ```product_grid.twig``` ,```top_picks_products.twig``` , ```bestseller-section.twig``` , ```products-selected.twig``` , ```home-featured-products-section.twig``` , ```section_products.twig``` , ```home-columns-products.twig```
* The supported products moudule keys are ```products``` , ```last_products```
* The supported products list in the moudule key is ```products```
* The supported products title key is ```name``` , ```name```
* The supported products display key is ```display``` it must be boolean if null we will consider it as true
* The supported products url key is ```url```
* The supported products module type key is ```module_type```
* The supported products id key is ```id``` it may used if the products related with one category
* The supported products more button object key is ```more_button``` and contains the ```text``` and ```url```

<img width="1086" alt="image" src="https://user-images.githubusercontent.com/45198998/236617803-3ab62113-25e2-44b3-ae35-dc12a5781c78.png">
<img width="1102" alt="image" src="https://user-images.githubusercontent.com/45198998/236618576-ec0e6fdd-1cea-4afc-8342-898edf0bb535.png">

## Category Module
* The supported file names : ```category-products-section.twig``` , ```home-category-products.twig``` , ```home-products-section.twig```
* The supported catgory moudule key is ```category```
* The supported category id key is ```id``` it used for moving to category page
* The supported category name key is ```name```
* The supported products in the moudule key is ```products```
* The supported category display more button key is ```display_more``` it must be boolean if null we will consider it as true

<img width="1101" alt="image" src="https://user-images.githubusercontent.com/45198998/236617910-a5d36428-c604-4971-b0f1-082346435de9.png">


## Categories Module
* The supported file names : ```category-section.twig``` , ```template-velvet-category-section.twig``` , ```home-categories.twig``` , ```categories.twig``` , ```categories_banner.twig``` , ```categories-selected.twig``` , ```home-categories-section.twig```
* The supported main title keys are ```title``` , ```sectionTitle``` , ```banner_title``` , 
* The supported sub title key is ```sectionSubTitle``` , ```desc```
* The supported categories display more button key is ```display_more``` it must be boolean if null we will consider it as false
* The supported more text button key is ```more_text```
* The supported cateogries items keys are ```categories``` , ```category_items``` the first one the category object must be named with ```category``` but in the last one the category object must be named with ```item``` 

<img width="1100" alt="image" src="https://user-images.githubusercontent.com/45198998/236676289-aca039f5-1f09-462e-8e2a-b2de653262a8.png">


## Categories with Products Module
* The supported file names : ```product-category.twig``` , ```home-tabs-section.twig```
* The supported moudule key is ```products``` and must contains a category object named ```category``` and contains products with list named ```products```
* The supported main title key is ```title``` , ```banner_title```
* The supported categories display more button key is ```display_more``` it must be boolean if null we will consider it as false


## Instagram Moudule
* The supported file names : ```instagram-gallery.twig``` 
* The supported main title key is ```title```
* The supported instagram username account key is ```instagram_account```
* The supported images list key is ```instagram``` and every object must contains ```image``` and ```url```

<img width="1035" alt="image" src="https://user-images.githubusercontent.com/45198998/236616926-82a7a11a-a658-4b42-aa0d-5a1519ae79d3.png">


## Banner Moudule
* The supported file names : ```banner.twig``` , ```large-banner.twig``` , ```big-banner.twig``` , ```image-with-text.twig``` , ```banner_img.twig```
* The supported banner image keys are ```mobile_image``` , ```image_mobile``` , ```image``` , ```banner_mobile_image``` , ```banner_image``` , ```img_banner``` , ```image```
* The supported banner link keys are ```url``` , ```link``` , ```banner_link```
* The supported banner background color key is ```color``` , ```banner_background_color``` if null we will use white color
* The supported banner title key is ```title``` , ```banner_title``` , ```sub_title``` , ```banner_des```
* The supported banner sub title keys are ```subtitle``` , ```des``` , ```desc```
* The supported banner title text color key is ```text_color``` if null we will use white color
* The supported banner button visibility key is ```show_button``` it should be boolean if null we will consider it as true
* The supported banner button title keys are ```button_text``` , ```button``` , ```btn_text```
* The supported banner button text color key is ```button_text_color``` , ```btn_text_color``` if null we will use white color
* The supported banner button background color key is ```button_bg_color``` , ```button_color``` , ```btn_background_color``` if null we will use primary color

<img width="1100" alt="image" src="https://user-images.githubusercontent.com/45198998/236676630-7659d407-a90b-42c5-bb88-e7249c8861f1.png">


## Brand Moudule
* The supported file names : ```home-brands-section.twig``` , ```home-brands.twig```
* The supported brand list key is ```brands```
* The supported brand list title key is ```title```
* The supported brand item image key is ```image``` , ```img```
* The supported brand item title key is ```title```
* The supported brand item url keys are ```url``` , ```link``` , ```url_button``` , ```video_link```

<img width="1106" alt="image" src="https://user-images.githubusercontent.com/45198998/236624662-0af9a0dd-88fb-4040-bdef-a3eeb2332ce6.png">


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
* The suppotted phone link key must be as ```phone``` in ```items``` in ```social_media``` in ```footer```
* The suppotted email link key must be as ```email``` in ```items``` in ```social_media``` in ```footer```
  
<img width="1097" alt="image" src="https://user-images.githubusercontent.com/45198998/236625722-e60bb15a-bebf-4530-8cef-8c2213f8ab32.png">


## FAQs Moudule
* The supported file names : ```home-faqs-section.twig```
* The supported FAQs list key is ```faqs_store_features``` and every object should contains ```title``` and ```answer```
* The supported FAQs background color key is ```details_bg``` if null we will use white color
* The supported FAQs video image key is ```details_video_img```
* The supported FAQs video url key is ```details_video``` should be a youtube video url
* The supported FAQs title key is ```details_title```
* The supported FAQs description key is ```details_desc```

<img width="1097" alt="image" src="https://user-images.githubusercontent.com/45198998/236624954-d0f3cb0e-4fb4-4fba-b4cf-28dd8bdd52c6.png">


## Testimonials Moudule
* The supported file names : ```testimonials.twig``` , ```home-reviews-section.twig``` , ```home-testimonials-section.twig```
* The supported testimonials list keys are ```testimonials``` , ```testimonial``` , ```reviews```
* The supported main description keys are ```des``` , ```desc```, ```sub_title``` , ```banner_des```
* The supported main title keys are ```title``` , ```title_offer``` , ```sectionTitle``` , ```banner_title```
* The supported testimonial item title keys are ```name``` , ```client_name``` , ```customer_name``` , ```customerName``` , ```author```
* The supported testimonial item date key is ```date```
* The supported testimonial item title keys are ```text``` , ```reviews``` , ```client_opinion``` , ```content``` , ```customerReview```

<img width="1105" alt="image" src="https://user-images.githubusercontent.com/45198998/236625663-4490817c-0668-4cec-a314-de8a4aba6e88.png">


## Partners Moudule
* The supported file names : ```partners.twig```
* The supported partners list key is ```store_partners```
* The supported main title key is ```title``` , ```banner_title```
* The supported main description key is ```des``` , ```desc```, ```sub_title``` , ```banner_des```
* The supported partner item image key is ```image``` , ```img```
* The supported partner url image keys are ```url``` , ```link```

<img width="1101" alt="image" src="https://user-images.githubusercontent.com/45198998/236625570-b49ff53d-d5d3-4547-9b63-374e42a54a05.png">


## Video Moudule
* The supported file names : ```video.twig```
* The supported video url key is ```video``` , ```banner_video```
* The supported control buttons visibility key is ```controls``` , ```banner_controls```
* The supported auto play key is ```autoplay``` , ```banner_autoplay``` it should be boolean if null we will consider it as false
* The supported main title key is ```title``` , ```banner_title```

<img width="1096" alt="image" src="https://user-images.githubusercontent.com/45198998/236626449-c2f888fc-765f-4188-aa85-8aab2e7d0425.png">


## Countdown Moudule
* The supported file names : ```countdown_banner.twig```
* The supported countdown date key is ```countdownDate```
* The supported countdown banner key is ```countdownImage``` it should be a list of object named ```image```



## Icon Box Moudule
* The supported file names : ```icon_box.twig```
* The supported icons box list key is ```infos```
* The supported icon box key is ```icon```
* The supported icon box title key is ```title```
* The supported icon box description key is ```description```


