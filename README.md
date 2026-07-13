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

## Common Section Keys (apply to every module)

Every home section is parsed through a unified component model, so the following keys work in **any** section's `settings` unless stated otherwise:

* Visibility: ```display``` boolean (default: true, accepts `"1"`/`"true"`), ```hide``` boolean (accepts `"1"`/`"true"`/`"on"`), ```hide_element``` boolean — when true the whole section is skipped
* Ordering: ```order```
* Title keys: ```title```, ```banner_title```, ```section_title```, ```sectionTitle```, ```title_offer```, ```heading```, ```image_title```, ```name```, ```tab_title```, ```main_title```, ```title1```, ```question```, ```faq```, ```title_text```
* Description keys: ```description```, ```subtitle```, ```sub_title```, ```small_subtitle```, ```sectionSubTitle```, ```des```, ```desc```, ```section_description```, ```text```, ```content```, ```answer```, ```subtitle_text```
* Link keys: ```url```, ```link```, ```url_button```, ```video_link```, ```primary_button_url```, ```banner_link```, ```button_url```, ```sectionBannerLink```, ```image_link```
* Mobile image keys: ```mobile_image```, ```image_mobile```, ```img_slider_mobile```, ```src_mobile```, ```background_image_mobile```, ```background_image_sm```, ```img_mobile```
* Image keys: ```image```, ```img```, ```img_slider```, ```img_banner```, ```background_image```, ```DesktopImage```
* Background image keys: ```background_banner```, ```background_image```
* Poster keys: ```poster_image```, ```poster```
* Alt text key: ```alt```
* Badge keys: ```badge_text```, ```badge```
* Button text keys: ```btn_text```, ```button_text```, ```buttonText```, ```text_button```, ```primary_button_text```, ```urltext```
* Secondary button keys: ```secondary_button_text```, ```secondary_button_url```
* "View more" keys: ```display_more``` boolean, ```more_text```, ```more_clr```, ```btn_url``` (fallbacks: ```more_url```, ```button_url```, ```more_link``` — providing ```more_link``` alone implies ```display_more: true```)
* Text color keys: ```text_color```, ```textColor```, ```color```
* Title color keys: ```title_color```, ```main_title_clr```, ```title_section_clr```, ```title_feature_clr```, ```title_feature_color```, ```cat_title_color```, ```text_color```, ```desColor```
* Description color keys: ```desc_section_clr```, ```color_description```, ```content_feature_clr```, ```content_feature_color```, ```des_color```, ```desc_clr```, ```desColor```, ```desc_color```, ```text_color```
* Subtitle color keys: ```sub_title_clr```, ```subtitle_color``` (plus background: ```main_title_bg_clr```, ```sub_title_bg_clr```)
* Background color keys: ```background_color```, ```bg_color```, ```bg_clr```, ```bg_section```, ```bg_clr_features```, ```bg_clr_feature```, ```bg_color_feature```, ```bg_clr_partners```, ```bg_clr_testimonsals```, ```section_background```
* Button color keys: ```button_color```, ```button_bg_clr```, ```button_bg_color```, ```btn_background_color```; button text color: ```button_text_color```, ```buttonTextColor```, ```btn_text_color```
* Style keys: ```product_style```, ```cat_style```, ```banner_type```, ```style_variant```, ```layout```
* Layout keys: ```container_type```, ```display_mode```, ```text_alignment```, ```position_title```, ```position_content```, ```background_position```, ```transition_effect```, ```overlay_opacity``` (0–100), ```min_height_mobile```, ```min_height_desktop```, ```border_color```, ```border_width```
* Items-per-row keys: ```number_on_sm``` (fallbacks: ```number_sm```, ```numberOnSm```, ```items_sm```), ```number_on_md``` (```numberOnMd```, ```items_md```), ```number_on_lg``` (```numberOnLg```, ```items_lg```)
* Slider behavior keys: ```hide_dots```, ```show_dots```, ```hide_navs```, ```autoplay``` (fallbacks: ```autoplay_enabled```, ```auto_play```, ```auto_move```), ```autoplay_delay```
* Alignment keys: ```title_center``` boolean, or ```title_align```/```titleAlign```/```title_alignment``` set to `"center"`
* Other behavior keys: ```show_as_column``` (fallbacks: ```show_column```, ```as_column```, ```is_vertical```), ```show_on_mobile```, ```hide_on_mobile```, ```show_button```, ```full_btn_border```, ```show_social```, ```controls```
* Section banner keys: ```section_banner```/```sectionBanner```, ```section_banner_link```/```sectionBannerLink```
* Side banner keys (products layouts): ```display_side_banner```, ```banner_show_mob```, ```banner_image```, ```banner_title```, ```banner_link```, ```banner_link_text```
* Sidebar keys (flat in settings): ```sideBar_title```, ```sideBar_desc```, ```sideBar_image```, ```sideBar_link```, ```sideBar_btn_text```, ```sideBar_text_color```, ```sideBar_desc_color```, ```options_design```

**Generic items list**: when a section carries a list under any of these keys, its objects are parsed as sub-items with the same key conventions above: ```main_slider```, ```slider```, ```slides```, ```spicial_slider```, ```gallery```, ```ads```, ```banners```, ```banner_grid```, ```features```, ```store_features```, ```partners```, ```store_partners```, ```brands_style_2```, ```testimonials```, ```testimonial```, ```reviews```, ```occasion_images```, ```tabs```, ```instagram```, ```infos```, ```faqs_store_features```, ```faqs```, ```FAQs```, ```questions_cart```, ```brands```, ```items```

---

## 1. Slider Module
* Supported file names: ```main-slider.jinja```, ```main_slider2.jinja```, ```slider.jinja```, ```sslider.jinja```, ```img-slider.jinja```, ```templete-velvet-main-slider.jinja```, ```slider_img.jinja```, ```carousel.jinja```, ```cards-slider-section.jinja```, ```spicial-slider.jinja```, ```slider-imgs.jinja```
* Supported slider items list keys: ```main_slider```, ```slider```, ```slides```, ```spicial_slider```
* Supported hide dots key: ```hide_dots``` boolean
* Supported autoplay keys: ```autoplay```, ```autoplay_enabled```, ```auto_play```, ```auto_move``` boolean (default: false); delay: ```autoplay_delay```
* Supported item type key: ```type```, ```slider_type``` — must be ```video``` or ```image``` (default: image)
* Supported item image keys: ```mobile_image```, ```image_mobile```, ```image```, ```img_slider_mobile```, ```img_slider```, ```background_image_mobile```, ```background_image_sm```, ```src_mobile```, ```background_image```, ```img_mobile```
* Supported item title keys: ```title```, ```heading```, ```image_title```
* Supported item subtitle keys: ```subtitle```, ```sub_title```, ```des```, ```desc```, ```description```
* Supported item badge text key: ```badge_text```, ```badge```
* Supported item overlay opacity key: ```overlay_opacity``` (number 0–100)
* Supported item text alignment key: ```text_alignment``` (start, center, end)
* Supported item button text keys: ```btn_text```, ```text_button```, ```button_text```, ```primary_button_text```
* Supported item secondary button text key: ```secondary_button_text```
* Supported item secondary button url key: ```secondary_button_url```
* Supported item text color key: ```text_color```, ```textColor``` (default: white)
* Supported item button background color key: ```background_color```, ```button_color```, ```button_bg_clr``` (default: primary)
* Supported item button text color key: ```button_text_color```, ```buttonTextColor```
* Supported item link keys: ```url```, ```link```, ```url_button```, ```video_link```, ```primary_button_url```, ```button_url```
* Supported item alt text key: ```alt```
* Supported background color key: ```background_color```
* Supported text color key: ```text_color```
* Supported title color key: ```title_color```
* Supported min height keys: ```min_height_mobile```, ```min_height_desktop```
* Supported transition effect key: ```transition_effect```

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
* Supported file names: ```gallery.jinja```, ```ggallery.jinja```, ```template-velvet-gallery.jinja```, ```home-banners-section.jinja```, ```grid-images.jinja```, ```image-group.jinja```
* Supported gallery items list keys: ```gallery```, ```ads```
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```sectionTitle```, ```heading```
* Supported grid layout keys: ```num_of_cols``` (columns), ```gap``` (spacing), ```border_radius```, ```custom_height```, ```enable_custom_height``` boolean
* Supported vertical layout key: ```show_as_column``` boolean (fallbacks: ```show_column```, ```as_column```, ```is_vertical```)
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
    ],
    "num_of_cols": 2,
    "gap": 8,
    "border_radius": 12
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
* Supported file names: ```products.jinja```, ```offers.jinja```, ```products-section.jinja```, ```product_grid.jinja```, ```top_picks_products.jinja```, ```bestseller-section.jinja```, ```products-selected.jinja```, ```home-featured-products-section.jinja```, ```section_products.jinja```, ```home-columns-products.jinja```, ```custom_product.jinja```, ```fixed-products.jinja```, ```products-display-section.jinja```, ```featured-product-section.jinja```, ```spicial-products.jinja```, ```banner-with-products.jinja```, ```products-with-bg.jinja```, ```products-slider.jinja```, ```products-grid.jinja```, ```products-grid-hor.jinja```
* Supported products block keys: ```products```, ```products_category```, ```category```, ```results```, ```tab_products```, ```productsCategory```
* Supported products list keys inside the block: ```results```, ```products```, ```data```, ```items``` — each item may also be wrapped under ```products``` (Zid) or ```product``` (Unaizah Pro)
* Supported title keys: ```title```, ```title_offer```, ```section_title```, ```sectionTitle```, ```banner_title```, ```heading```
* Supported display key: ```display``` boolean (default: true)
* Supported display more key: ```display_more``` boolean (```more_link``` alone also enables it)
* Supported more text keys: ```more_text```; more url keys: ```btn_url```, ```more_url```, ```button_url```, ```more_link```
* Supported more text color key: ```more_clr```, ```more_text_color```
* Supported url key: ```url```
* Supported module type key: ```module_type```
* Supported id key: ```id```
* Supported description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description``` — for ```fixed-products.jinja``` / ```spicial-products.jinja``` also ```small_text```, ```small_title```
* Supported description color key: ```desc_section_clr```, ```description_color```
* Supported title color keys: ```title_section_clr```, ```title_color```
* Supported background section color key: ```bg_section```
* Supported container type key: ```container_type```, ```display_type```, ```image_direction```
* Supported number per row key: ```number_on_sm``` (fallbacks: ```number_sm```, ```numberOnSm```, ```items_sm```), ```number_on_md```, ```number_on_lg```
* Supported hide dots key: ```hide_dots``` (setting it to ```false``` shows dots on horizontal lists)
* Supported title center key: ```title_center``` (or ```title_align: "center"```)
* Supported section banner keys: ```section_banner```/```sectionBanner```, ```section_banner_link```/```sectionBannerLink```
* Supported side banner keys: ```display_side_banner``` boolean, ```banner_image```, ```banner_title```, ```banner_link```, ```banner_link_text```, ```banner_show_mob```
* Supported more button border color key: ```border_button_color```

> **Notes:**
> * ```products-section.jinja``` with no title and no ```small_subtitle```/```small_text```/```small_title``` is hidden entirely.
> * ```banner-with-products.jinja``` renders a media banner above a header-less grid; ```products-with-bg.jinja``` renders the grid over a full-bleed background image.
> * ```home-columns-products.jinja``` supports the multi-category ```nest``` list — each entry wraps its own ```products``` block and renders as an independent block.

```json
{
  "settings": {
    "title": "منتجات متميزة",
    "products": {
      "results": [],
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
* Supported category module key: ```category``` — the section title and "view all" link are read from ```settings.category.name``` and ```settings.category.url```
* Supported category id key: ```id```
* Supported category name key: ```name```
* Supported products key: ```products```
* Supported display more key: ```display_more``` boolean (default: true)
* Supported more text keys: ```more_text```

---

## 6. Categories Module
* Supported file names: ```category-section.jinja```, ```template-velvet-category-section.jinja```, ```home-categories.jinja```, ```categories.jinja```, ```categories_banner.jinja```, ```categories-selected.jinja```, ```home-categories-section.jinja```, ```categories-list.jinja```, ```category-list.jinja```, ```images-square.jinja```, ```category-style2.jinja```, ```category-style3.jinja```, ```categories-section.jinja```
* Supported main title keys: ```title```, ```sectionTitle```, ```section_title```, ```banner_title```, ```heading```
* Supported subtitle keys: ```sectionSubTitle```, ```desc```
* Supported display more key: ```display_more``` boolean
* Supported more text keys: ```more_text```; more url keys: ```btn_url```, ```more_url```, ```more_link```
* Supported more text color key: ```more_clr```, ```more_text_color```
* Supported categories items keys: ```categories```, ```category_items```, ```category```, ```images_square``` — each item may be wrapped under ```category```, ```selectedCategory```, or ```item```
* Supported card-style items key: ```category_style2``` (card layouts used by ```category-style2.jinja``` / ```category-style3.jinja```)
* Supported category style key: ```cat_style``` (fallbacks: ```product_style```, ```banner_type```, ```style_variant```)
* Supported container type key: ```container_type```, ```display_type```, ```image_direction```
* Supported number of items keys: ```number_on_sm```, ```number_on_md```, ```number_on_lg```
* Supported hide dots key: ```hide_dots```
* Supported hide navigation key: ```hide_navs```
* Supported title center key: ```title_center```
* Supported title color key: ```title_section_clr```
* Supported description color key: ```desc_section_clr```, ```description_color```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_section```
* Supported border button color key: ```border_button_color```

---

## 7. Categories with Products Module (Products Tabs)
* Supported file names: ```product-category.jinja```, ```home-tabs-section.jinja```, ```products_grid_tabs.jinja```, ```products-tab.jinja```, ```tabs-products.jinja```, ```multi-products.jinja```, ```products-grid-tabs.jinja```
* Supported tabs list keys: ```products_categories```, ```tab_products```, ```categories```, ```tabs```
* Each tab supports: ```category``` object (with ```id```, ```name```/```label```, ```url```, ```products```/```results```), ```display_more``` boolean, ```more_url```, ```more_text```, ```max``` (cap on rendered products; 0 = no cap)
* Alternative tab shape: ```tab_title``` + ```tab_products``` (products payload with ```url```)
* Alternative multi-box shape (```multi-products.jinja```): ```box1_name```/```box1_products``` up to ```box10_name```/```box10_products``` — each ```boxN_products``` holds ```results```
* Unaizah Pro tab shape: ```title``` + ```listProducts``` (`category` or `selected`) + ```productsCategory``` object or inline ```products``` list (items wrapped under ```product```)
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported title color key: ```title_color```
* Supported more text color key: ```more_clr```, ```more_text_color```
* Supported border button color key: ```border_button_color```

> **Note:** If the category ```id``` is missing, it is extracted automatically from the category ```url``` (e.g. ```/categories/1415209/...```).

---

## 8. Instagram Module
* Supported file names: ```instagram-gallery.jinja```, ```instagram.jinja```
* Supported main title key: ```title```
* Supported instagram username key: ```instagram_account```
* Supported images list keys: ```instagram``` or ```images``` — every object must contain ```image``` and ```url```

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
* Supported file names: ```banner.jinja```, ```large-banner.jinja```, ```big-banner.jinja```, ```image-with-text.jinja```, ```banner_img.jinja```, ```hero.jinja```, ```banner-image.jinja```, ```banner-text.jinja```, ```banner-grid.jinja```, ```banners.jinja```, ```ad_image.jinja```
* Supported image keys: ```mobile_image```, ```image_mobile```, ```image```, ```img_banner```, ```background_image_mobile```, ```background_image```
* Supported background image key: ```background_banner```
* Supported link keys: ```url```, ```link```, ```banner_link```, ```button_url```
* Supported background color keys: ```color```, ```background_color```, ```bg_color``` (default: white)
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported subtitle keys: ```subtitle```, ```sub_title```, ```des```, ```desc```, ```description```, ```section_description```
* Supported badge text key: ```badge_text```
* Supported overlay opacity key: ```overlay_opacity``` (0–100)
* Supported text color keys: ```text_color```, ```textColor``` (default: white)
* Supported button visibility key: ```show_button``` boolean (default: true)
* Supported button text keys: ```button_text```, ```btn_text```, ```primary_button_text```
* Supported button text color keys: ```button_text_color```, ```btn_text_color``` (default: white)
* Supported button bg color keys: ```button_bg_color```, ```button_color```, ```btn_background_color``` (default: primary)
* Supported container type key: ```container_type```

**Multi-image layouts:**
* ```banners.jinja``` — a wrap grid of images. Grid keys: ```banners``` (items list), ```banners_per_row```, ```banners_per_row_mobile```, ```stack_banners_mobile``` boolean
* ```banner-grid.jinja``` — one large banner followed by a row of smaller banners (items under ```banner_grid```), each with gradient, title and CTA
* Any unmapped section that carries an items list **and** the ```banners_per_row``` key is automatically rendered as a banners grid

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
    "overlay_opacity": 30
  }
}
```

---

## 10. Brand Module
* Supported file names: ```home-brands-section.jinja```, ```home-brands.jinja```, ```brands.jinja```, ```brands-style-2.jinja```
* Supported brand list keys: ```brands``` (a plain list, or an object ```{ "title", "display", "items": [...] }```), ```brands_style_2```
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading``` (or ```brands.title```)
* Supported subtitle key: ```small_text```
* Supported brand item image keys: ```image```, ```img```
* Supported brand item title key: ```title```
* Supported brand item url keys: ```url```, ```link```, ```url_button```, ```video_link```

---

## 11. Description / About Module
* Supported file names: ```store-description.jinja```, ```logo-social.jinja```, ```about-us.jinja```
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported subtitle key: ```sub_title```, ```subtitle```
* Supported description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description```
* Supported image key: ```image```
* Supported title color key: ```title_color```
* Supported button keys: ```btn_text```, ```btn_url```
* Supported min height mobile key: ```min_height_mobile```
* Supported social media visibility key: ```show_social``` boolean
* Supported display key: ```display``` boolean
* Social media links are loaded from the store settings (```social_media_*``` keys — see Global Settings)

---

## 12. FAQs Module
* Supported file names: ```home-faqs-section.jinja```, ```home-faqs.jinja```, ```faq.jinja```, ```faqs.jinja```, ```yasmeen-faqs.jinja```, ```faq-section.jinja```
* Supported FAQs list keys: ```faqs_store_features```, ```faqs```, ```FAQs```, ```questions_cart```
* Supported item question keys: ```title```, ```question```, ```faq```
* Supported item answer keys: ```answer```, ```content```, ```text```, ```description```
* Supported store FAQs key: ```showStoreFaqs``` boolean — when true, the store's global FAQ list is shown instead of the section's own items
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
* Supported main description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description```
* Supported main title color key: ```main_title_clr```
* Supported title position key: ```position_title```, ```position_content```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_clr_testimonsals```, ```background_color```, ```section_background```
* Supported hide dots key: ```hide_dots```
* Supported item name keys: ```name```, ```client_name```, ```customer_name```, ```customerName```, ```author```
* Supported item image keys: ```client_image```, ```image```
* Supported item date key: ```date```
* Supported item review text keys: ```text```, ```reviews```, ```client_opinion```, ```content```, ```customerReview```, ```des```
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
* Supported main description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description```
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
* Supported video url key: ```video```
* Supported controls visibility key: ```controls```
* Supported autoplay keys: ```autoplay```, ```autoplay_enabled```, ```auto_play```, ```auto_move``` boolean (default: false)
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported description keys: ```description```, ```des```, ```desc```
* Supported link key: ```url```
* Supported poster image keys: ```poster_image```, ```poster```
* Supported image key: ```image```

> **Note:** YouTube URLs are automatically detected and rendered with a YouTube player.

---

## 16. Countdown Module
* Supported file names: ```countdown_banner.jinja```, ```countdown-banner.jinja```, ```countdown.jinja```
* Supported countdown date keys: ```expiry_date```, ```end_date```, ```countdownDate``` — supported formats: ```yyyy-MM-dd HH:mm:ss```, ```yyyy/M/d```, ```yyyy-MM-dd```
* Supported countdown image keys: ```countdownImage``` (list of objects with ```image```), ```image```, ```offer_image```, ```background_image_mobile```, ```background_image```, ```background_image_sm```, or an ```occasion_images``` list
* Supported occasion toggle key: ```occasion_enable```
* Supported title/description/badge keys: ```title```, ```description```, ```badge_text``` (common fallbacks apply)
* Supported button keys: ```btn_text```, ```btn_url``` (falls back to ```url```)

---

## 17. Icon Box Module
* Supported file names: ```icon_box.jinja```, ```icon-box.jinja```
* Supported icons box list key: ```infos```
* Supported icon key: ```icon```
* Supported title key: ```title```
* Supported description key: ```description```

---

## 18. Trust Payment Module
* Supported file names: ```trust_payment.jinja```
* Supported visibility key: ```show_on_mobile``` boolean — only displayed when true
* Payment methods are loaded from store settings

---

## 19. Announcement Bar Module
* Loaded from global store settings (not from individual module settings)
* Supported display key: ```announcement_bar_display``` (or inverse ```news_hide```)
* Supported text keys: ```announcement_bar_text```, ```announcement_bar_title```
* Supported announcements list: ```announcement_bar_announcements``` (objects with ```title```/```name```, ```url```/```link```, ```image```/```img```, ```icon```)
* Supported multi-text lists: ```news_items``` (objects with ```title```), ```announcement_bar_texts``` (objects with ```text```), ```news``` (objects with ```title```)
* Supported advertisement list: ```announcement_bar_advertisement_bar``` (image + text marquee items)
* Supported link key: ```announcement_bar_url```
* Supported background color keys: ```announcement_bar_background_color```, ```announcement_bar_BackgroundColor```, ```announcement_bar_BgColor```, ```news_bg```
* Supported text color keys: ```announcement_bar_text_color```, ```announcement_bar_TextColor```, ```news_text```
* Supported font size keys: ```announcement_bar_TextFontSize```, ```announcement_bar_text_font_size```
* Supported behavior keys: ```announcement_bar_move```, ```announcement_bar_stop_move```, ```announcement_bar_text_marquee```, ```announcement_bar_enable_animation```, ```announcement_bar_pause_on_hover```, ```announcement_bar_animation_speed```, ```announcement_bar_autoplaySpeed```/```announcement_bar_autoplay_speed```, ```announcement_bar_page_display```

---

## 20. Advertisement Bar Module
* Supported file names: ```advertisement-bar.jinja``` (rendered as an image + text marquee strip)
* Supported visibility key: ```hide_element``` boolean
* Supported items list key: ```advertisement_bar```
* Supported item image keys: ```image```, ```img```
* Supported item title keys: ```title```, ```name```
* Supported item url keys: ```url```, ```link```
* Supported background color key: ```background_color```
* Supported marquee stop key: ```stop_move``` boolean

```json
{
  "settings": {
    "advertisement_bar": [
      { "image": "https://example.com/ad.png", "title": "عرض خاص", "url": "/offers" }
    ],
    "background_color": "#ffffff",
    "stop_move": false
  }
}
```

---

## 21. Quick Links Module
* Supported file names: ```quick-links.jinja```
* Supported items list key: ```items``` — each item must contain ```image```; supported link keys: ```url```, ```link```
* Supported main title key: ```title```
* Supported small subtitle key: ```small_subtitle```
* Supported two-rows layout key: ```swiper_two_rows_mobile``` boolean — splits the tiles over two horizontally scrolling rows

---

## 22. Branches Module
* Supported file names: ```branches.jinja```
* Supported branches list keys: ```branches```, ```locations```
* Supported item keys: ```name```, ```address```, ```phone```
* Supported main title key: ```title```

---

## 23. Compare Content Module
* Supported file names: ```compare-content.jinja```
* Supported image keys: ```image_1```, ```image_2```
* Supported label keys: ```title_1```, ```title_2```
* Supported additional text key: ```additional_text```
* Supported main title key: ```title```; title color: ```title_color```
* Supported link keys: ```url```, ```btn_url```

---

## 24. Informative Module
* Supported file names: ```informative.jinja```
* Supported items list key: ```informative_box```
* Supported main image key: ```main_image```
* Supported main title key: ```title```
* Supported subtitle keys: ```small_subtitle```, ```small_text```
* Supported item image/title keys: ```image```, ```title``` (common fallbacks apply)
* Supported item description keys: ```des```, ```desc```, ```description```

---

## 25. Text Section Module
* Supported file names: ```text-section.jinja```
* Supported text keys: ```text``` (single) or ```textList``` (list of texts)
* Supported text style keys: ```textColor```, ```textSize```, ```textWeight```
* Supported marquee keys: ```textMove``` boolean, ```textSpeed```
* Supported background keys: ```bgView```, ```bgColor```, ```bgColor2```, ```bgGradient```, ```bgImage```
* Supported icon key: ```icon```
* Supported link keys: ```url```, ```link```
* Supported spacing keys: ```height```, ```topSpace```, ```bottomSpace```, ```spaceStyle```, ```textSpace```, ```itemPadding```

---

## 26. Video Stories Module
* Supported file names: ```video-stories.jinja```, ```products-video-slider.jinja```
* Supported items list key: ```videos``` — each item contains ```video``` (URL) and optional ```product``` object
* Supported autoplay key: ```autoplayVideos``` boolean
* Supported section title keys: ```sectionTitle```, ```sectionSubTitle```
* Supported titles style keys: ```titlesStyle_titleColor```, ```titlesStyle_titleSize```, ```titlesStyle_titleWeight```, ```titlesStyle_titleAlign```, ```titlesStyle_subTitleColor```, ```titlesStyle_subTitleSize```, ```titlesStyle_subTitleWeight```
* Supported background keys: ```bgColor```, ```bgColor2```, ```bgGradient```
* Supported spacing keys: ```topSpace```, ```bottomSpace```

---

## 27. Video Slider Module
* Supported file names: ```video-slider.jinja```
* Supported items list key: ```content``` — each item contains ```video```, optional ```product``` object, ```title```, ```text```
* Supported layout keys: ```view```, ```videoHeight```
* Supported product card keys: ```hideATC``` (hide add-to-cart), ```hidePrice```, ```hideArrow```, ```productBgColor```, ```productNameColor```
* Supported section title keys: ```sectionTitle```, ```sectionSubTitle```
* Supported titles style keys: ```titlesStyle_titleColor```, ```titlesStyle_titleSize```, ```titlesStyle_titleWeight```, ```titlesStyle_titleAlign```, ```titlesStyle_subTitleColor```, ```titlesStyle_subTitleSize```, ```titlesStyle_subTitleWeight```
* Supported background keys: ```bgColor```, ```bgColor2```, ```bgGradient```
* Supported spacing keys: ```topSpace```, ```bottomSpace```, ```spaceStyle```

---

## 28. Blogs Module
* Supported file names: ```home-blog.jinja```, ```blogs.jinja```, ```blog.jinja```
* Supported blogs list keys: ```blog```, ```blogs```
* Supported main title key: ```title```
* Supported item image keys: ```image```, ```img```
* Supported item title keys: ```title```, ```text```
* Supported item url key: ```url```
* Supported item button text key: ```btn_text```

---

## 29. Points Products Module
* Supported file names: ```points-products.jinja```
* The section is recognized by the app but is intentionally not rendered inside the home screen (loyalty points products are handled by the app's native loyalty module).

------------------------

## Global Settings Keys Reference

The app parses the store-wide theme settings into structured sections. All keys below live at the settings root.

### Colors (`colors_*`)
| Key | Usage |
|---|---|
| ```colors_background_image``` | Page background image |
| ```colors_bg_color``` / ```colors_bg_color_mobile``` | Background color |
| ```colors_text_color``` / ```colors_text_color_mobile``` | Text color |
| ```colors_icons_color``` / ```colors_icons_color_mobile``` | Icons color |
| ```colors_page_background_color``` | Page background |
| ```colors_header_background_color``` / ```colors_header_text_color``` | Header colors |
| ```colors_header_menu_background_color``` / ```colors_header_menu_text_color``` | Header menu colors |
| ```colors_footer_background_color``` / ```colors_footer_text_color``` | Footer colors |
| ```colors_menu_text_color``` / ```colors_menu_title_color``` | Menu colors |

### Fonts (`fonts_*`)
| Key | Fallback | Usage |
|---|---|---|
| ```fonts_name``` | ```basic_font``` | Custom font name |
| ```fonts_font_style``` | — | Font style |
| ```fonts_font_url``` | — | Custom font URL |
| ```fonts_font_weight``` | ```basic_fontWeight``` | Font weight |
| ```fonts_customfont``` | — | Enable custom font |

### Header (`header_*`)
| Key | Usage |
|---|---|
| ```header_logo``` / ```header_logo_mobile``` / ```header_logo_after_scroll``` / ```header_logo_white``` | Store logos |
| ```header_width_logo``` / ```header_logo_width_desktop``` / ```header_logo_width_mobile``` / ```header_contral_logo_size_manually``` | Logo sizing |
| ```header_sticky``` / ```header_transparent_header``` / ```header_setting_transparent_header``` | Header behavior |
| ```header_setting_header_style_2``` / ```header_setting_mega_menu``` / ```header_setting_navigation_bar``` / ```header_setting_show_all_categories``` | Header options |
| ```header_header_background_color``` / ```header_header_text_color``` / ```header_overlay_header_text_color``` | Header colors (fallbacks: ```colors_header_*```) |
| ```header_header_shape_desktop``` / ```header_header_shape_mobile``` | Header shape |
| ```header_search_placeholder``` / ```header_hide_search_bar``` | Search bar |
| ```header_hide_country``` / ```header_hide_language``` | Locale switchers |
| ```header_colors_bg_header``` / ```header_colors_bg_header_mobile``` / ```header_colors_bg_header_icons``` | Header bg colors |
| ```header_colors_icon_cart_color``` / ```header_colors_icon_country_color``` / ```header_colors_icon_lang_color``` / ```header_colors_icon_user_color``` | Header icon colors |
| ```header_options``` | Options list |

### Footer (`footer_*`)
| Key | Usage |
|---|---|
| ```footer_settings_footer_logo``` / ```footer_settings_logo_width_desktop``` / ```footer_settings_logo_width_mobile``` | Footer logo |
| ```footer_settings_background_color``` (fallbacks: ```footer_colors_bg_clr_footer```, ```footer_style_bg_clr_footer```, ```colors_footer_background_color```) | Footer background |
| ```footer_settings_text_color``` (fallbacks: ```footer_colors_clr_text_footer```, ```colors_footer_text_color```) | Footer text |
| ```footer_colors_clr_title_footer``` / ```footer_style_des_clr``` | Footer title/description colors |
| ```footer_style_social_background``` / ```footer_style_social_color``` | Social icon colors |
| ```footer_settings_footer_style``` / ```footer_setting_center_content``` | Footer style |
| ```footer_copyright_store_copyright``` | Copyright text |
| ```footer_setting_contact_us``` / ```footer_setting_shipping_icons``` | Footer options |
| ```footer_settings_hide_about``` / ```footer_settings_hide_business_address``` / ```footer_settings_hide_contact``` / ```footer_settings_hide_language_currency_switcher``` / ```footer_settings_hide_legal``` / ```footer_settings_hide_links_1``` / ```footer_settings_hide_links_2``` / ```footer_settings_hide_payment``` / ```footer_settings_hide_shipping``` / ```footer_settings_hide_social_media``` | Footer visibility toggles |

### Links Groups
| Key | Fallback | Usage |
|---|---|---|
| ```links_1_title``` / ```links_1_links``` / ```links_1_hide``` | ```links_links1Title``` / ```links_links1List``` / ```links_links1Show``` | Links group 1 |
| ```links_2_*```, ```links_3_*```, ```links_4_*``` | ```links_links2*``` … | Links groups 2–4 |
| ```links_title``` / ```links_links``` / ```links_display_vertical``` / ```links_menulogo``` | — | Generic single group |

Each link item supports: ```title```/```name```, ```url```/```link```, ```image```/```img```, ```icon```.

### Menu (`menu_*`)
| Key | Usage |
|---|---|
| ```menu_settings_links``` / ```menu_settings_markat``` | Menu link lists |
| ```menu_settings_main_menu_options``` | Main menu options |
| ```menu_settings_hide_markat``` / ```menu_settings_hide_payment``` | Menu visibility |
| ```menu_settings_show_all_porducts``` / ```menu_settings_show_main_category``` / ```menu_settings_show_main_menu_mobile``` | Menu visibility |
| ```menuHideDiscount``` / ```menu_hide_discount``` | Hide discount badge |
| ```menu_show_categories_mobile``` | Show categories mobile |
| ```navigation_options``` | Navigation options list |

### Menu Icons & Categories
| Key | Usage |
|---|---|
| ```MenuIcons_allProducts``` / ```MenuIcons_allCategories``` / ```MenuIcons_newestProducts``` / ```MenuIcons_onSaleProducts``` / ```MenuIcons_CustomLinks``` / ```MenuIcons_DeliveryAndPayment``` / ```MenuIcons_ShoppingCart``` | Menu icons |
| ```MenuCategories_allCategories``` | Show all categories |
| ```MenuCategories_categoriesList``` | Selected categories (items with ```selectedCategory.id```) |
| ```MenuCategories_categoriesImagesIcons``` | Category images/icons |

### About Us (`about_us_*`)
| Key | Fallback |
|---|---|
| ```about_us_title``` | — |
| ```about_us_description``` | ```about_us_des```, ```about_us_desc``` |
| ```about_us_img``` / ```about_us_width_img``` | — |
| ```about_us_footer_logo``` | ```about_us_footerlogo``` |
| ```about_us_android_app_link``` / ```about_us_apple_app_link``` | — |

### Social Media (`social_media_*`)
| Key | Usage |
|---|---|
| ```social_media_title``` | Section title |
| ```social_media_facebook``` / ```social_media_twitter``` / ```social_media_instagram``` / ```social_media_snapchat``` / ```social_media_tiktok``` / ```social_media_youtube``` / ```social_media_website_or_youtube``` | Social links |
| ```social_media_whatsapp_number``` (fallback: ```whatsapp_whatsapp_number```) | WhatsApp number |
| ```social_media_email``` / ```social_media_show_email``` / ```social_media_show_phone``` / ```social_media_show_whatsapp``` | Contact toggles |

### Product Card (`product_card_*`)
| Key | Usage |
|---|---|
| ```product_card_style``` / ```product_card_product_card_style``` / ```product_card_product_card_text_style``` | Card style |
| ```product_card_text_direction``` / ```product_card_product_card_text_direction``` | Text direction |
| ```product_card_image_style``` / ```product_card_product_card_image_style``` / ```product_card_img_fit``` / ```product_card_image_size_object_fit``` / ```product_card_image_size_aspect_ratio``` | Image style |
| ```product_card_img_height``` / ```product_card_img_height_small``` / ```product_card_img_border_radius``` / ```product_card_border_radius``` | Sizing |
| ```product_card_gap_between_products``` (fallback: ```product_card_gap_bettwen_products```) | Grid gap |
| ```product_card_colors_card_background_color``` / ```product_card_colors_card_border_color``` / ```product_card_colors_title_color``` | Card colors |
| ```product_card_colors_add_to_cart_background_color``` / ```product_card_colors_add_to_cart_text_color``` | Add-to-cart colors |
| ```product_card_discount_display``` / ```product_card_another_img``` | Display options |
| ```product_card_hide_add_to_cart``` / ```product_card_hide_add_to_wishlist``` / ```product_card_hide_quick_view``` / ```product_card_hide_rating``` | Visibility toggles |

### General (`general_*`)
| Key | Usage |
|---|---|
| ```general_back_top``` | Back-to-top button |
| ```general_border_radius_buttons_border_radius``` / ```general_border_radius_form_inputs_border_radius``` / ```general_border_radius_genral_border_radius``` | Border radii |
| ```general_localization_hide_currency_selector``` / ```general_localization_hide_destination_selector``` / ```general_localization_hide_lang_selector``` | Localization toggles |
| ```general_product_card_image_mode``` | Product image mode |
| ```general_settings_height_img_product_lg``` / ```general_settings_height_img_product_sm``` / ```general_settings_height_img_product_2_lg``` / ```general_settings_height_img_product_2_sm``` | Product image heights |
| ```general_settings_line_clamp``` / ```general_settings_public_img_size``` / ```general_whatsapp``` | Misc |

### Chat & WhatsApp Buttons
| Key | Usage |
|---|---|
| ```chat_btn_display``` / ```chat_btn_background_color``` / ```chat_btn_icon_color``` | Chat button |
| ```chat_btn_contacts_list_email``` / ```chat_btn_contacts_list_phone``` / ```chat_btn_contacts_list_whatsapp``` / ```chat_btn_contacts_list_telegram``` | Chat contacts |
| ```WAButton_active``` / ```WAButton_BgColor``` / ```WAButton_phone``` / ```WAButton_direction``` / ```WAButton_isCircle``` / ```WAButton_position``` | WhatsApp floating button |

### Splash & PWA
| Key | Usage |
|---|---|
| ```splash_screen_display``` / ```splash_screen_background_color``` / ```splash_screen_page_display``` | Splash screen |
| ```splash_screen_show_loader``` / ```splash_screen_loader_type``` / ```splash_screen_loader_colors_loader_color``` | Splash loader |
| ```pwa_app_background_color``` / ```pwa_app_theme_color``` / ```pwa_pwa_install_banner_display``` | PWA settings |

------------------------

## Advanced: Per-Section Rendering Overrides (`entaj_props`)

Any home section may include an ```entaj_props``` object (at the section root, next to ```settings```) to fine-tune how the Apps Bunches app renders that specific section — spacing, fonts, colors, layout details, etc. These keys are applied on top of the theme defaults and are app-specific (they do not affect the web theme). Contact us at Dev@AppsBunches.com for the full list of override keys per section.

------------------------

If you have any inquiries, feel free to contact us directly via email at Dev@AppsBunches.com
