## Introduction
* Welcome to the Apps Bunches عناقيد التطبيقات Recommendations for Zid Theme Developers! This guide helps developers seamlessly integrate Zid themes with the Apps Bunches mobile application [App Link](https://apps.zid.sa/application/421).

## By following these recommendations, developers can ensure:
* Seamless Integration: Structured file naming and key conventions for effortless compatibility.
* Consistent User Experience: Maintaining visual coherence across different theme components.
* Optimized Performance: Enhancing loading speed and responsiveness within the app.
* Error-Free Development: Reducing potential issues by following predefined standards.
------------

> ### ⚠️ Important Note for Theme Developers
> This document lists all file names using the **`.jinja`** extension, which is the standard for **Vitrin themes**.
> However, the Apps Bunches mobile application fully supports **both** Vitrin themes (`.jinja`) and legacy themes (`.twig`).
>
> **If you are developing a legacy theme**, simply replace `.jinja` with `.twig` in all file names listed below — the supported keys and JSON structure remain exactly the same.
>
> | Theme Type | File Extension | Example |
> |---|---|---|
> | **Vitrin (New)** | `.jinja` | `main-slider.jinja` |
> | **Legacy** | `.twig` | `main-slider.twig` |

If you have any inquiries, feel free to reach out to us at Dev@AppsBunches.com 

----------------

## 1. Slider Module
* Supported file names: ```main-slider.jinja```, ```main_slider2.jinja```, ```slider.jinja```, ```sslider.jinja```, ```img-slider.jinja```, ```templete-velvet-main-slider.jinja```, ```slider_img.jinja```, ```carousel.jinja```
* Supported slider items list keys: ```slider```, ```slides```
* Supported hide dots key: ```hide_dots``` boolean (default: true)
* Supported autoplay key: ```autoplay```, ```autoplay_enabled``` boolean (default: false)
* Supported item type key: ```type```, ```slider_type``` — must be ```video``` or ```image``` (default: image)
* Supported item image keys: ```mobile_image```, ```image_mobile```, ```image```, ```img_slider_mobile```, ```img_slider```, ```background_image_mobile```, ```src_mobile```, ```background_image```
* Supported item title keys: ```title```, ```heading```, ```image_title```
* Supported item subtitle keys: ```subtitle```, ```sub_title```, ```des```, ```desc```, ```description```
* Supported item badge text key: ```badge_text```
* Supported item overlay opacity key: ```overlay_opacity``` (number 0–100)
* Supported item text alignment key: ```text_alignment``` (start, center, end)
* Supported item button text keys: ```btn_text```, ```text_button```, ```button_text```, ```primary_button_text```
* Supported item secondary button text key: ```secondary_button_text```
* Supported item secondary button url key: ```secondary_button_url```
* Supported item text color key: ```text_color```, ```textColor``` (default: white)
* Supported item button background color key: ```background_color```, ```button_color``` (default: primary)
* Supported item button text color key: ```button_text_color```, ```buttonTextColor```
* Supported item link keys: ```url```, ```link```, ```url_button```, ```video_link```, ```primary_button_url```, ```button_url```
* Supported item alt text key: ```alt```
* Supported background color key: ```background_color```
* Supported text color key: ```text_color```
* Supported title color key: ```title_color```
* Supported min height mobile key: ```min_height_mobile```

```json
{
  "settings": {
    "slider": [
      {
        "title": "عنوان على الصورة",
        "des": "النص على الصورة",
        "image": "https://example.com/image.png",
        "url": "/products/example",
        "badge_text": "جديد",
        "overlay_opacity": 50,
        "text_alignment": "center",
        "btn_text": "تسوق الآن",
        "text_color": "#ffffff",
        "type": "image"
      }
    ],
    "background_color": "#ff6c40",
    "text_color": "#fff5f5",
    "hide_dots": false,
    "autoplay": true
  }
}
```

---

## 2. Gallery Module
* Supported file names: ```gallery.jinja```, ```ggallery.jinja```, ```template-velvet-gallery.jinja```, ```home-banners-section.jinja```, ```grid-images.jinja```
* Supported gallery items list keys: ```gallery```, ```ads```
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```sectionTitle```, ```heading```
* Supported item image keys: ```image```, ```img```, ```src_mobile```, ```image_mobile```, ```background_image```
* Supported item link keys: ```url```, ```link```, ```url_button```, ```video_link```, ```primary_button_url```, ```button_url```
* Supported item title keys: ```title```, ```heading```, ```image_title```
* Supported item subtitle keys: ```subtitle```, ```sub_title```, ```des```, ```desc```, ```description```
* Supported item button visibility key: ```show_button``` boolean (default: true)
* Supported item border-only button key: ```full_btn_border``` boolean (default: false)
* Supported item button text keys: ```btn_text```, ```button_text```, ```buttonText```, ```text_button```, ```primary_button_text```
* Supported item secondary button text key: ```secondary_button_text```
* Supported item secondary button url key: ```secondary_button_url```
* Supported item text color key: ```text_color```, ```textColor``` (default: white)
* Supported item button color key: ```button_color```, ```background_color``` (default: primary)
* Supported item alt text key: ```alt```

```json
{
  "settings": {
    "gallery": [
      {
        "image": "https://example.com/image.jpg",
        "title": "عنوان",
        "subtitle": "وصف",
        "text_color": "#ffffff",
        "show_button": true,
        "full_btn_border": true,
        "button_text": "اضغط هنا",
        "button_color": "#ff0000",
        "url": "/products/example",
        "alt": "وصف الصورة"
      }
    ]
  }
}
```

---

## 3. Features Module
* Supported file names: ```features.jinja```, ```store-features.jinja```, ```features-section.jinja```, ```benefits.jinja```
* Supported feature items list keys: ```features```, ```store_features```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_section```, ```bg_clr_features```, ```background_color```, ```section_background``` (default: white)
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported main title color key: ```main_title_clr```
* Supported main description keys: ```des```, ```desc```, ```sub_title```, ```subtitle```, ```description```, ```section_description```
* Supported item image keys: ```image_mobile```, ```image```, ```img```, ```icon``` (must not be null)
* Supported item title keys: ```title```, ```text```
* Supported item description keys: ```des```, ```desc```, ```description```
* Supported item text color key: ```text_color``` (default: black)
* Supported feature title color key: ```title_feature_clr```, ```title_feature_color```
* Supported feature content color key: ```content_feature_clr```, ```content_feature_color```
* Supported feature individual bg color key: ```bg_clr_feature```, ```bg_color_feature```
* Supported title position key: ```position_title```, ```position_content```
* Supported container type key: ```container_type```, ```display_type```, ```image_direction```

```json
{
  "settings": {
    "title": "مميزاتنا",
    "features": [
      {
        "image": "https://example.com/icon.png",
        "text": "طرق دفع متعددة",
        "desc": "وصف الميزة",
        "text_color": "#ff0000"
      }
    ],
    "bg_color": "#481229",
    "main_title_clr": "#ffffff"
  }
}
```

---

## 4. Products Module
* Supported file names: ```products.jinja```, ```offers.jinja```, ```products-section.jinja```, ```product_grid.jinja```, ```top_picks_products.jinja```, ```bestseller-section.jinja```, ```products-selected.jinja```, ```home-featured-products-section.jinja```, ```section_products.jinja```, ```home-columns-products.jinja```, ```custom_product.jinja```
* Supported products module keys: ```products```, ```last_products```
* Supported products list in the module key: ```products```
* Supported title keys: ```title```, ```title_offer```, ```section_title```, ```sectionTitle```, ```banner_title```, ```heading```
* Supported display key: ```display``` boolean (default: true)
* Supported display more key: ```display_more``` boolean
* Supported more text keys: ```more_text```, ```more_button_text```, ```more_button```
* Supported more text color key: ```more_clr```, ```more_text_color```
* Supported url key: ```url```
* Supported module type key: ```module_type```
* Supported id key: ```id```
* Supported description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description```
* Supported description color key: ```desc_section_clr```, ```description_color```
* Supported title color keys: ```title_section_clr```, ```title_color```
* Supported background section color key: ```bg_section```
* Supported container type key: ```container_type```, ```display_type```, ```image_direction```
* Supported number per row key: ```number_on_sm```, ```number_on_md```, ```number_on_lg```
* Supported hide dots key: ```hide_dots```
* Supported title center key: ```title_center```
* Supported section banner key: ```sectionBanner```
* Supported section banner link key: ```sectionBannerLink```
* Supported more button border color key: ```border_button_color```

```json
{
  "settings": {
    "title": "منتجات متميزة",
    "products": {
      "products": [],
      "module_type": "sale_products",
      "url": "/categories/123/"
    },
    "display_more": true,
    "more_text": "استكشف المزيد",
    "number_on_sm": 2,
    "hide_dots": false,
    "title_center": true
  }
}
```

---

## 5. Category Products Module
* Supported file names: ```category-products-section.jinja```, ```home-category-products.jinja```, ```home-products-section.jinja```
* Supported category module key: ```category```
* Supported category id key: ```id```
* Supported category name key: ```name```
* Supported products key: ```products```
* Supported display more key: ```display_more``` boolean (default: true)
* Supported more text keys: ```more_text```, ```more_button_text```, ```more_button```

---

## 6. Categories Module
* Supported file names: ```category-section.jinja```, ```template-velvet-category-section.jinja```, ```home-categories.jinja```, ```categories.jinja```, ```categories_banner.jinja```, ```categories-selected.jinja```, ```home-categories-section.jinja```
* Supported main title keys: ```title```, ```sectionTitle```, ```section_title```, ```banner_title```, ```heading```
* Supported subtitle keys: ```sectionSubTitle```, ```desc```
* Supported display more key: ```display_more``` boolean (default: false)
* Supported more text keys: ```more_text```, ```more_button_text```, ```more_button```
* Supported more text color key: ```more_clr```, ```more_text_color```
* Supported categories items keys: ```categories```, ```category_items``` — first uses ```category``` object, second uses ```item```
* Supported category style key: ```cat_style```
* Supported container type key: ```container_type```, ```display_type```, ```image_direction```
* Supported number of items keys: ```number_on_sm```, ```number_on_md```, ```number_on_lg```
* Supported hide dots key: ```hide_dots```
* Supported hide navigation key: ```hide_navs```
* Supported title center key: ```title_center```
* Supported title color key: ```title_section_clr```
* Supported description color key: ```desc_section_clr```, ```description_color```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_section```
* Supported border button color key: ```border_button_color```
* Supported hide category names key: ```hide_category_names```

---

## 7. Categories with Products Module (Custom Products Tabs)
* Supported file names: ```product-category.jinja```, ```home-tabs-section.jinja```, ```products_grid_tabs.jinja```
* Supported module key: ```products``` — must contain ```category``` object with ```products``` list
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported display more key: ```display_more``` boolean (default: false)
* Supported more text keys: ```more_text```, ```more_button_text```, ```more_button```
* Supported title color key: ```title_color```
* Supported more text color key: ```more_clr```, ```more_text_color```
* Supported border button color key: ```border_button_color```

**Products Grid Tabs format (```products_grid_tabs.jinja```):**
* ```tab_1_products``` to ```tab_4_products``` — each is a list of objects containing ```products```
* ```tab_1_title``` to ```tab_4_title``` — titles for each tab

---

## 8. Instagram Module
* Supported file names: ```instagram-gallery.jinja```
* Supported main title key: ```title```
* Supported instagram username key: ```instagram_account```
* Supported images list key: ```instagram``` — every object must contain ```image``` and ```url```

```json
{
  "settings": {
    "title": "تسوق عبر الانستجرام",
    "instagram_account": "store_name",
    "instagram": [
      { "image": "https://example.com/photo.jpg", "url": "/products/example" }
    ]
  }
}
```

---

## 9. Banner Module
* Supported file names: ```banner.jinja```, ```large-banner.jinja```, ```big-banner.jinja```, ```image-with-text.jinja```, ```banner_img.jinja```, ```hero.jinja```, ```banner-image.jinja```
* Supported image keys: ```mobile_image```, ```image_mobile```, ```image```, ```banner_mobile_image```, ```banner_image```, ```img_banner```, ```background_image_mobile```, ```background_image```
* Supported link keys: ```url```, ```link```, ```banner_link```, ```button_url```
* Supported background color keys: ```color```, ```banner_background_color``` (default: white)
* Supported background banner color key: ```background_banner```
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported subtitle keys: ```subtitle```, ```sub_title```, ```des```, ```desc```, ```description```, ```banner_des```, ```section_description```
* Supported badge text key: ```badge_text```
* Supported overlay opacity key: ```overlay_opacity``` (0–100)
* Supported text color keys: ```text_color```, ```textColor```, ```banner_text_color``` (default: white)
* Supported text position key: ```text_position_right``` boolean
* Supported button visibility key: ```show_button``` boolean (default: true)
* Supported button text keys: ```button_text```, ```button```, ```btn_text```, ```primary_button_text```
* Supported button text color keys: ```button_text_color```, ```btn_text_color``` (default: white)
* Supported button bg color keys: ```button_bg_color```, ```button_color```, ```btn_background_color``` (default: primary)
* Supported container type key: ```container_type```, ```display_type```

```json
{
  "settings": {
    "title": "عنوان البانر",
    "subtitle": "وصف البانر",
    "image": "https://example.com/banner.jpg",
    "mobile_image": "https://example.com/banner-mobile.jpg",
    "text_color": "#ffffff",
    "show_button": true,
    "button_text": "اضغط هنا",
    "button_bg_color": "#ff0000",
    "button_text_color": "#ffffff",
    "url": "/categories/123",
    "text_position_right": true,
    "overlay_opacity": 30
  }
}
```

---

## 10. Brand Module
* Supported file names: ```home-brands-section.jinja```, ```home-brands.jinja```
* Supported brand list key: ```brands```
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported brand item image keys: ```image```, ```img```
* Supported brand item title key: ```title```
* Supported brand item url keys: ```url```, ```link```, ```url_button```, ```video_link```

---

## 11. Description Module
* Supported file names: ```store-description.jinja```, ```logo-social.jinja```
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description```
* Supported image key: ```image```
* Supported title color key: ```title_color```
* Supported description color key: ```desc_color2```
* Supported min height mobile key: ```min_height_mobile```
* Supported social media visibility key: ```display_social_media``` boolean
* Supported display key: ```display``` boolean
* Social media links are loaded from ```footer.social_media.items``` (keys: ```tiktok```, ```twitter```, ```instagram```, ```facebook```, ```snapchat```, ```phone```, ```email```)

---

## 12. FAQs Module
* Supported file names: ```home-faqs-section.jinja```, ```faq.jinja```, ```faqs.jinja```
* Supported FAQs list keys: ```faqs_store_features```, ```faqs```, ```questions_cart``` — each object should contain ```title``` and ```answer```
* Supported background color key: ```details_bg``` (default: white)
* Supported video image key: ```details_video_img```
* Supported video url key: ```details_video``` (YouTube URL)
* Supported title key: ```details_title```
* Supported description key: ```details_desc```

---

## 13. Testimonials Module
* Supported file names: ```testimonials.jinja```, ```home-reviews-section.jinja```, ```home-testimonials-section.jinja```
* Supported testimonials list keys: ```testimonials```, ```testimonial```, ```reviews```
* Supported main title keys: ```title```, ```title_offer```, ```sectionTitle```, ```section_title```, ```banner_title```, ```heading```
* Supported main description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```banner_des```, ```section_description```
* Supported main title color key: ```main_title_clr```
* Supported title position key: ```position_title```, ```position_content```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_clr_testimonsals```, ```background_color```, ```section_background```
* Supported hide dots key: ```hide_dots```
* Supported button color key: ```button_bg_color```, ```button_color```
* Supported icon color key: ```icon_color```
* Supported item name keys: ```name```, ```client_name```, ```customer_name```, ```customerName```, ```author```
* Supported item date key: ```date```
* Supported item review text keys: ```text```, ```reviews```, ```client_opinion```, ```content```, ```customerReview```
* Supported item rating key: ```rating``` (numeric, displayed as stars)

```json
{
  "settings": {
    "title": "آراء العملاء",
    "testimonials": [
      {
        "name": "اسم العميل",
        "date": "منذ 5 أيام",
        "text": "رأي العميل",
        "rating": 5
      }
    ],
    "bg_color": "#f5f5f5",
    "hide_dots": false
  }
}
```

---

## 14. Partners Module
* Supported file names: ```partners.jinja```
* Supported partners list keys: ```store_partners```, ```partners```
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported main description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```banner_des```, ```section_description```
* Supported title color key: ```main_title_clr```
* Supported title position key: ```position_title```
* Supported background color key: ```bg_clr_partners```
* Supported number per row key: ```number_on_sm```
* Supported hide dots key: ```hide_dots```
* Supported hide navigation key: ```hide_navs```
* Supported item image keys: ```image```, ```img```
* Supported item url keys: ```url```, ```link```

---

## 15. Video Module
* Supported file names: ```video.jinja```, ```video-or-Image.jinja```, ```video-product-section.jinja```
* Supported video url keys: ```video```, ```banner_video```
* Supported controls visibility keys: ```controls```, ```banner_controls```
* Supported autoplay keys: ```autoplay```, ```banner_autoplay```, ```autoplay_enabled``` boolean (default: false)
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported poster image key: ```poster_image```
* Supported image key: ```image```

> **Note:** YouTube URLs are automatically detected and rendered with a YouTube player.

---

## 16. Countdown Module
* Supported file names: ```countdown_banner.jinja```, ```countdown.jinja```
* Supported countdown date keys: ```countdownDate```, ```end_date```, ```expiry_date``` (format: yyyy/M/d)
* Supported countdown image keys: ```countdownImage``` (list of objects with ```image```), ```offer_image```, ```background_image_mobile```, ```background_image```, ```background_image_sm```

---

## 17. Icon Box Module
* Supported file names: ```icon_box.jinja```
* Supported icons box list key: ```infos```
* Supported icon key: ```icon```
* Supported title key: ```title```
* Supported description key: ```description```

---

## 18. Trust Payment Module
* Supported file names: ```trust_payment.jinja```
* Supported visibility key: ```show_on_mobile``` boolean — only displayed when true
* Payment methods are loaded from store settings (```footer.paymentMethods```)

---

## 19. Announcement Bar Module
* Loaded from global store settings (not from individual module settings)
* Supported display key: ```announcement_bar_display```, ```news_hide```
* Supported text key: ```announcement_bar_text```
* Supported text from announcements: ```announcement_bar_announcements``` (array — first item's ```text```)
* Supported link key: ```announcement_bar_url``` (or first ```announcement_bar_announcements``` item's ```url```)
* Supported marquee key: ```announcement_bar_move``` boolean
* Supported background color keys: ```announcement_bar_background_color```, ```announcement_bar_bgcolor```, ```bannerBackgroundColor```, ```news_bg```
* Supported text color keys: ```announcement_bar_text_color```, ```announcement_bar_textcolor```, ```bannerTextColor```

---

## 20. Advertisement Bar Module
* Supported visibility key: ```hide_element``` boolean
* Supported items list key: ```advertisement_bar```
* Supported item image keys: ```image```, ```img```
* Supported item title key: ```title```
* Supported item url keys: ```url```, ```link```
* Supported background color keys: ```background_color```, ```banner_background_color```

```json
{
  "settings": {
    "hide_element": false,
    "advertisement_bar": [
      { "image": "https://example.com/ad.png", "title": "عرض خاص", "url": "/offers" }
    ],
    "background_color": "#ffffff"
  }
}
```

---

## 21. Banner Slider Module
* Supported banner sliders list key: ```bannerSliders```
* Each item contains: ```text``` and ```link```
* Supported background color keys: ```announcement_bar_background_color```, ```bannerBackgroundColor```
* Supported text color keys: ```announcement_bar_text_color```, ```bannerTextColor```
* Supported banner height key: ```bannerHeight```

---

## 22. Availability Bar Module
* Loaded from global store settings
* Displays when the store is closed (```closedNow``` and ```isStoreClosed``` both true)
* Message loaded from ```settings.availability.message```

---

## Global Settings Keys Reference

### Colors
| Key | Fallback Keys | Usage |
|---|---|---|
| ```text_color``` | ```textColor```, ```color```, ```banner_text_color``` | Text color |
| ```title_color``` | ```text_color``` | Title color |
| ```bg_color``` | ```bg_clr```, ```bg_section```, ```bg_clr_testimonsals```, ```bg_clr_features```, ```text_bg```, ```background_color```, ```section_background``` | Background |
| ```button_text``` | ```button```, ```btn_text``` | Button label |
| ```button_bg_color``` | ```button_color```, ```btn_background_color``` | Button background |
| ```button_text_color``` | ```btn_text_color``` | Button text color |
| ```options_design``` | — | Design variant |
| ```fonts_name``` | — | Custom font |

### Links and Navigation
| Key | Fallback Keys | Usage |
|---|---|---|
| ```links_1_links``` | ```links_urls```, ```links_links```, ```link_groups_items[0].links``` | Footer links 1 |
| ```links_2_links``` | ```links2_links``` | Footer links 2 |
| ```links3_links``` | ```links_3_links``` | Footer links 3 |
| ```links_1_title``` | ```links_title``` | Links 1 title |
| ```menu_settings_links``` | ```links_1_links```, ```header_links_menu```, ```main_menu_links``` | Menu links |

### Menu Icons
| Key | Usage |
|---|---|
| ```MenuIcons_allProducts``` | All products icon |
| ```MenuIcons_allCategories``` | All categories icon |
| ```MenuIcons_newestProducts``` | Newest products icon |
| ```MenuIcons_onSaleProducts``` | On sale icon |
| ```MenuIcons_CustomLinks``` | Custom links icon |
| ```MenuIcons_DeliveryAndPayment``` | Delivery icon |
| ```MenuIcons_ShoppingCart``` | Cart icon |

### Menu Options
| Key | Usage |
|---|---|
| ```menuHideDiscount``` / ```menu_hide_discount``` | Hide discount badge |
| ```menu_settings_show_all_porducts``` | Show all products |
| ```menu_settings_show_main_menu_mobile``` | Show main menu mobile |
| ```menu_settings_show_main_category``` | Show main category |
| ```menu_settings_hide_markat``` | Hide markat |
| ```menu_show_categories_mobile``` | Show categories mobile |

### Header / Footer Colors
| Key | Usage |
|---|---|
| ```colors_header_background_color``` | Header background |
| ```colors_header_text_color``` | Header text |
| ```colors_footer_background_color``` | Footer background |
| ```colors_footer_text_color``` | Footer text |
| ```header_logo``` | Store logo URL |

### About Us
| Key | Fallback Keys |
|---|---|
| ```about_us_title``` | ```about_title``` |
| ```about_us_des``` | ```about_des```, ```about_us_about_us``` |

------------------------

If you have any inquiries, feel free to contact us directly via email at Dev@AppsBunches.com
