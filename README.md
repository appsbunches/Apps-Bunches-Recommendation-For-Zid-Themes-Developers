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

```
{
    "modules": [
        {
            "id": "81373ec6-8590-4141-b9da-944f4f902036",
            "storefront_theme_store_id": "93baacfe-19ee-4c66-a3da-9c5f702aaed3",
            "storefront_theme_file_id": "7de183cb-df6b-411f-b3f5-7f65f6ac7d",
            "settings": {
                "title": "منتجات متميزة",
                "products": [
                    {
                        "product": {}
                    },
                    {
                        "product": {}
                    },
                    {
                        "product": {}
                    }
                ],
                "display_more": true,
                "more_text": "استكشف المزيد ",
                "order": 7
            },
            "is_draft": 0,
            "draft_for": null,
            "is_deleted": 0,
            "created_at": "2022-08-18T08:40:49.000000Z",
            "updated_at": "2022-08-18T08:41:49.000000Z"
        }
    ]
}
```
OR
```
{
    "modules": [
        {
            "id": "c8a997d6-dd0b-452e-ac69-7b71a776a940",
            "storefront_theme_store_id": "e63cOadb-5f1d-44cb-9e48-4be4b4065a2a",
            "storefront_theme_file_id": "d414294d-5b0f-4606-9611-32b8cebb5£64",
            "settings": {
                "title": "منتجات عليها عروض",
                "products": {
                    "products": [],
                    "module_type": "sale_products"
                },
                "display_more": true,
                "more_text": " عرض الكل عرض الكل عرض الكل",
                "order": 12
            },
            "is_draft": 0,
            "draft_for": null,
            "is_deleted": 0,
            "created_at": "2022-05-29T09:33:27.000000Z",
            "updated_at": "2023-02-11T19:01:03.000000Z"
        },
        {
            "id": "e087fa5d-1475-4bd0-be5c-5a58ee2bddc6",
            "storefront_theme_store_id": "e63c0adb-5f1d-44cb-9e48-4be4b4065a2a",
            "storefront_theme_file_id": "d414294d-5b0£-4606-9611-32b8cebb5£64",
            "settings": {
                "title": " منتجات عبد الله",
                "products": {
                    "products": [],
                    "url": "/categories/384063/",
                    "module_type": "products_category"
                },
                "more_text": " المزيد المزيد المزيد",
                "order": 9,
                "display_more": false
            }
        }
    ]
}
```
## Category Module
* The supported file names : ```category-products-section.twig``` , ```home-category-products.twig``` , ```home-products-section.twig```
* The supported catgory moudule key is ```category```
* The supported category id key is ```id``` it used for moving to category page
* The supported category name key is ```name```
* The supported products in the moudule key is ```products```
* The supported category display more button key is ```display_more``` it must be boolean if null we will consider it as true

```
{
    "modules": [
        {
            "id": "2137bd1c-6094-49ff-9641-953c5b31a3db",
            "storefront_theme_store_id": "41460ab1-bbbf-4c59-bb06-542575a4e59a",
            "storefront_theme_file_id": "Ob0db37a-7a94-478b-ab8f-bde1912736e2",
            "settings": {
                "category": {
                    "id": 361590,
                    "name": "حلاوة المانوكا",
                    "حلاوة- المانوكا ": "slug",
                    "SE0_category_title": "حلاوة المانوكا",
                    "SE0_category_description": "حلاوة المانوكا",
                    "description": null,
                    "url": "https://1du1fk.zidthemestore.com/categories/361590/LejLaJI=ögX",
                    "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/eaa78£77-17e3-4ed9-85d£-24e96312d66b-260x260.png",
                    "image_full_size": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/eaa78f77-17e3-4ed9-85df-24e96312d66b.png",
                    "img_alt_text": null,
                    "cover_image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/38514574-a5e6-4cda-a5b1-310699548f42.png",
                    "products_count": 0,
                    "sub_categories": [],
                    "parent_id": null,
                    "is_published": true,
                    "products": [],
                    "module_type": "category_products"
                },
                "display_more": true,
                "more_text": "عرض الكل",
                "order": 5
            }
        }
    ]
}
```

## Categories Module
* The supported file names : ```category-section.twig``` , ```template-velvet-category-section.twig``` , ```home-categories.twig``` , ```categories.twig``` , ```categories_banner.twig``` , ```categories-selected.twig``` , ```home-categories-section.twig```
* The supported main title keys are ```title``` , ```sectionTitle``` , ```banner_title``` , 
* The supported sub title key is ```sectionSubTitle``` , ```desc```
* The supported categories display more button key is ```display_more``` it must be boolean if null we will consider it as false
* The supported more text button key is ```more_text```
* The supported cateogries items keys are ```categories``` , ```category_items``` the first one the category object must be named with ```category``` but in the last one the category object must be named with ```item``` 

```
{
    "modules": [
        {
            "id": "728919e8-d1b9-4ead-8fa8-def9d4525e69",
            "storefront_theme_store_id": "41460ab1-bbbf-4c59-bb06-542575a4e59a",
            "storefront_theme_file_id": "572bc314-d75d-4781-88ea-3562b8а4420c",
            "settings": {
                "title": "أحدث التصنيفات",
                "categories": [
                    {
                        "category": {},
                    },
                    {
                        "category": {},
                    },
                    {
                        "category": {
                            "id": 361591,
                            "name": " بخاخ المانوكا",
                            "slug": "بخاخ - المانوكا",
                            "SEO_category_title": "بخاخ المانوكا",
                            "SE0_category_description": "بخاخ المانوكا",
                            "description": null,
                            "uz1": "https://1du1fk.zidthemestore.com/categories/361591/بخاخ - المانوكا",
                            "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/{1d87001-5e0c-478d-be82-fa426bbc4192-260x260.png",
                            "image_full_size": "https://media.zid.store/b2d{7841-8071-401e-8883-77C9cb7cd9a1/{1d87001-5e0c-478d-be82-fa426bbc4192.png",
                            "img_alt_text": null
                        }
                    }
                ]
            }
        }
    ]
}
```

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

```
{
    "modules": [
        {
            "id": "Oc4cbf90-efd5-49cb-b515-b5554f2f2b59",
            "storefront_theme_store_id": "e63c0adb-5f1d-44cb-9e48-4be4b4065a2a",
            "storefront_theme_file_id": "42d1455a-b2bf-49b7-b796-ebfe7d704876",
            "settings": {
                "title": "تسوق عبر الانتستجرام",
                "instagram_account": "teejangold",
                "instagram": [
                    {
                        "image": "https://media.zid.store/b2d{7841-8071-401e-8883-77c9cb7cd9a1/9035ffbd-f85f-4691-b837-b76e0807b673.jpg",
                        "urI": "/shipping-and-payment"
                    },
                    {
                        "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/093f362b-36de-4516-9de0-b68e16b3ab1d.jpg",
                        "url": "/faqs"
                    },
                    {
                        "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/£d3631ed-Oa8e-40c1-a84c-8489a6f221cb.jpg",
                        "url": "https://www.instagram.com/teejangold/"
                    },
                    {
                        "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/48688ef9-8e4f-4f03-909f-7b4327b338af.png",
                        "url": "https://www.youtube.com/"
                    },
                    {
                        "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/cc903a96-f2e9-48b8-9bd9-c5488d44c0c9.jpg",
                        "ur1": "/categories/445886/ .٣-محمود",
                        "order": 1
                    }
                ]
            }
        }
    ]
}
```

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

```
{
    "modules": [
        {
            "id": "432c7989-6b9a-4833-8d19-ab81383365a2",
            "storefront_theme_store_id": "e63c0adb-5f1d-44cb-9e48-4be4b4065a2а",
            "storefront_theme_file_id": "901c0446-2be9-4fc7-ac76-1af6а5585182",
            "settings": {
                "text_position_right": true,
                "title": "Abdallah Abdallah Abdallah ",
                "subtitle": "Much of the QA",
                "text_color":"#ffffff",
                "image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/54526c45-e854-4fa6-8180-d8d57b410ee9.jpg",
                "mobile_image": "https://media.zid.store/b2df7841-8071-401e-8883-77c9cb7cd9a1/{d3631ed-Oa8e-40c1-a84c-8489a6{221cb.jpg",
                "show_button": true,
                "button_text": "اضغط هنا",
                "button_bg_color": "#ff0000",
                "button_text_color": "#d1bffe",
                "url": "/categories/361591/ بخاخ - المانوك",
                "order": 2,
                "is_draft": 0,
                "draft_for": null,
                "is_deleted": 0,
                "created_at": "2022-05-25T07:28:24.000000z",
                "updated_at": "2022-09-03T17:28:46.000000Z"
            }
        }
    ]
}
```

## Brand Moudule
* The supported file names : ```home-brands-section.twig``` , ```home-brands.twig```
* The supported brand list key is ```brands```
* The supported brand list title key is ```title```
* The supported brand item image key is ```image``` , ```img```
* The supported brand item title key is ```title```
* The supported brand item url keys are ```url``` , ```link``` , ```url_button``` , ```video_link```

```
{
    "modules": [
        {
            "id": "02e4652e-7£55-457-bb78-4d298cfce7£4",
            "storefront_theme_store_id": "98fafeb0-5811-4c3f-8eef-8£91123aa2b9",
            "storefront_theme_file_id": "Oc270de5-5ecc-49c5-abaa-b585fe10cd13",
            "settings": {
                "bg_color": "#ffffff",
                "brands": [
                    {
                        "image": "https://media.zid.store/d8ecbdd2-Obfd-4172-88a9-69a512dc3e7d/dbaad4a3-9869-4£71-8fc2-d6067b£b27£7.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-0bfd-4172-88a9-69a512dc3e7d/9db7c6ce-1359-4db3-a1d8-2508c6b32187.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-Obfd-4172-88a9-69a512dc3e7d/6ff6e659-b6ab-4aec-ad9c-06ab266013ce.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-Obfd-4172-88a9-69a512dc3e7d/b4e34a34-c415-4421-8ee3-01086851cfae.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-0bfd-4172-88a9-69a512dc3e7d/a08cd79d-654a-4ece-9067-1be25fed5972.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-0bfd-4172-88a9-69a512dc3e7d/6e62cd9c-1a17-4d05-9370-46a875a73f99.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-0bfd-4172-88a9-69a512dc3e7d/8d1fd70e-053c-46dd-a36c-13d9fa652269.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-0bfd-4172-88a9-69a512dc3e7d/87d8f532-4952-4de2-90a5-709088d78d35.png"
                    },
                    {
                        "image": "https://media.zid.store/d8ecbdd2-0bfd-4172-88a9-69a512dc3e7d/6e6b2a7d-0f9e-47fb-896c-29895528b78b.jpg"
                    }
                ]
            }
        }
    ]
}
```

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

```
{
    "modules": [
        {
            "id": "301beaa9-8089-4c43-b0a3-cc1e32fa4aae",
            "storefront_theme_store_id": "e57a0654-7476-428b-b03b-db15c8bd9£41",
            "storefront_theme_file_id": "c39cc13C-af93-41fe-bf36-9a0c3a41a4e1",
            "settings": {
                "title": "وصف المتجر",
                "desc": "وصف عام للمتجر يبرز أهم المنتجات أو الخدمات التي يقدمها ",
                "display_social_media": true,
                "order": 1
            },
            "is_draft": 0,
            "draft_for": null,
            "is_deleted": 0,
            "created_at": "2023-02-19T17:27:14.000000Z",
            "updated_at": "2023-02-23T08:57:48. 000000Z"
        }
    ]
}
```
ــ

## FAQs Moudule
* The supported file names : ```home-faqs-section.twig```
* The supported FAQs list key is ```faqs_store_features``` and every object should contains ```title``` and ```answer```
* The supported FAQs background color key is ```details_bg``` if null we will use white color
* The supported FAQs video image key is ```details_video_img```
* The supported FAQs video url key is ```details_video``` should be a youtube video url
* The supported FAQs title key is ```details_title```
* The supported FAQs description key is ```details_desc```

```
{
    "modules": [
        {
            "id": "9e0f74b7-08b4-4d58-a946-af9199d30412",
            "storefront_theme_store_id": "98fafeb0-5811-4c3f-8eef-8f91123aa2b9",
            "storefront_theme_file_id": "Ebd6b44d-e05a-4541-a296-1cc4381addf5",
            "settings": {
                "details_title": "اسئلة متنوعة من عملائنا",
                "details_desc": "اسئلة العملاء",
                "details_bg": "#a7291f",
                "details_video": "https://youtu.be/zC_TbG6H1j0",
                "details_video_img": "https://media.zid.store/d8ecbdd2-Obfd-4172-88a9-69a512dc3e7d/b437b784-5ec6-4a9e-aOeb-88df59eee£50.png",
                "details_figure": "https://media.zid.store/d8ecbdd2-Obfd-4172-88a9-69a512dc3e7d/b2081369-69ef-4cf0-99d1-e473cc0582d1.png",
                "faqs_store_features": [
                    {
                        "title": "ما هي آلية الشحن والتوصيل؟",
                        "answer": ".لعملاء مدينة جدة تأكد من اتمام طلبك قبل الساعة الرابعة عصراً ليصلك الطلب في نفس اليوم"
                    },
                    {
                        "title": "ما الحل في حال تأخر الطلب ؟",
                        "answer": "في حال تأخر طلبك عن المدة المحددة للشحن"
                    }
                ],
                "order": 8,
                "is_draft": 0
            }
        }
    ]
}
```

## Testimonials Moudule
* The supported file names : ```testimonials.twig``` , ```home-reviews-section.twig``` , ```home-testimonials-section.twig```
* The supported testimonials list keys are ```testimonials``` , ```testimonial``` , ```reviews```
* The supported main description keys are ```des``` , ```desc```, ```sub_title``` , ```banner_des```
* The supported main title keys are ```title``` , ```title_offer``` , ```sectionTitle``` , ```banner_title```
* The supported testimonial item title keys are ```name``` , ```client_name``` , ```customer_name``` , ```customerName``` , ```author```
* The supported testimonial item date key is ```date```
* The supported testimonial item title keys are ```text``` , ```reviews``` , ```client_opinion``` , ```content``` , ```customerReview```

```
{
    "modules": [
        {
            "id": "82cdb3a1-649f-44c3-b448-315cdf£7d4d3",
            "storefront_theme_store_id": "e57a0654-7476-428b-b03b-db15c8bd9f41",
            "storefront_theme_file_id": "ba37b0d1-29d5-4948-a939-bea43a798d72",
            "settings": {
                "title": "آراء العملاء",
                "testimonials": [
                    {
                        "name": "اسم العميل",
                        "date": " أيام 5 منذ",
                        "text": " هنا يضع العميل رأيه أو تقييمه لتجربة الشراء من المتجر"
                    },
                    {
                        "name": "اسم العميل",
                        "date": " أيام 5 منذ",
                        "text": " هنا يضع العميل رأيه أو تقييمه لتجربة الشراء من المتجر"
                    },
                    {
                        "name": "اسم العميل",
                        "date": " أيام 5 منذ",
                        "text": " هنا يضع العميل رأيه أو تقييمه لتجربة الشراء من المتجر"
                    }
                ]
            }
        }
    ]
}
```

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


