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

Every home section is parsed through a unified component model, so the following keys work in **any** section's `settings` unless stated otherwise. Keys are listed in lookup order — the first key that carries a value wins.

* Visibility: ```display``` boolean (default: true, accepts `"1"`/`"true"`), ```hide``` boolean (accepts `"1"`/`"true"`/`"on"`), ```hide_element``` boolean — when true the whole section is skipped
* Ordering: ```order```
* Title keys: ```title```, ```banner_title```, ```section_title```, ```sectionTitle```, ```title_offer```, ```heading```, ```image_title```, ```name```, ```tab_title```, ```main_title```, ```title1```, ```question```, ```faq```, ```title_text```, ```title_sec```, ```title_section```, ```text_title```, ```label``` — when no title is set, a ```desc``` that differs from the description is used as the title
* Description keys: ```description```, ```subtitle```, ```sub_title```, ```small_subtitle```, ```sectionSubTitle```, ```title_offer_sub```, ```des```, ```desc```, ```section_description```, ```text```, ```content```, ```answer```, ```subtitle_text```, ```explain```, ```paragraph```
* Second paragraph keys (shown below the description): ```description_02```, ```desc_02```, ```description2```, ```sub_description```
* Kicker (small line above the title): ```small_subtitle```, ```kicker```; caption (small line below the title): ```small_text```
* Subtitle keys: ```sub_title```, ```subtitle```, ```count```
* Link keys: ```url```, ```link```, ```href```, ```url_button```, ```video_link```, ```primary_button_url```, ```banner_link```, ```button_url```, ```sectionBannerLink```, ```image_link```, ```view_all_url```, ```cta_link```, ```url_1```
* Mobile image keys: ```mobile_image```, ```image_mobile```, ```img_slider_mobile```, ```src_mobile```, ```background_image_mobile```, ```background_image_sm```, ```img_mobile```, ```image2```, ```mobimage```, ```mobile_poster```, ```mobile```
* Image keys: ```image```, ```img```, ```img_slider```, ```img_banner```, ```background_image```, ```DesktopImage```, ```desktop_poster```, ```image1```, ```custom_image```, ```desktop```, ```icon_image```, ```desktop_image```, ```image_desktop```, ```logo``` (the app is mobile, so the mobile image is preferred when both are sent)
* Background image keys: ```background_banner```, ```background_image```, ```backgroundimage```
* Section logo keys (shown beside the section title): ```logo```, ```logo_image```
* Poster keys: ```poster_image```, ```poster```
* Video keys: ```video```, ```video_upload```; mobile video: ```video_mobile```, ```mobile_video```
* Alt text key: ```alt```
* Badge keys: ```badge_text```, ```badge```, ```badge_label```, ```slogan```
* Countdown keys: ```expiry_date``` (fallbacks: ```end_date```, ```countdownDate```); text shown after expiry: ```message_expired``` (fallbacks: ```expired_message```, ```messageExpired```)
* Button text keys: ```btn_text```, ```button_text```, ```buttonText```, ```text_button```, ```primary_button_text```, ```urltext```, ```button```, ```url_title_1```, ```urlTitle```
* Secondary button keys: ```secondary_button_text```, ```secondary_button_url```
* "View more" keys:
  * Toggle: ```display_more``` boolean (fallbacks: ```showLoadMore```, ```show_load_more```, ```display_show_all```, ```show_view_all```, ```display_see_all```, ```show_all```)
  * Label: ```more_text``` (fallbacks: ```loadMoreText```, ```load_more_text```, ```view_all_text```, ```see_all_text```, ```btn```)
  * Link: ```btn_url``` (fallbacks: ```more_url```, ```button_url```, ```more_link```, ```view_all_url```, ```see_all_url```)
  * Color: ```more_clr```
  * When no toggle is sent, providing ```more_link``` or ```view_all_url```, or a non-empty "more" label, turns the button on
* Text color keys: ```text_color```, ```textColor```, ```color```, ```textcolor```
* Title color keys: ```title_color```, ```main_title_clr```, ```title_section_clr```, ```title_feature_clr```, ```title_feature_color```, ```cat_title_color```, ```text_color```, ```desColor```
* Description color keys: ```desc_section_clr```, ```color_description```, ```content_feature_clr```, ```content_feature_color```, ```des_color```, ```desc_clr```, ```desColor```, ```desc_color```, ```text_color```, ```texts_color```
* Subtitle color keys: ```sub_title_clr```, ```subtitle_color```, ```sub_title_color``` (plus background: ```main_title_bg_clr```, ```sub_title_bg_clr```)
* Background color keys: ```background_color```, ```bg_color```, ```bg_clr```, ```bg_section```, ```bg_clr_features```, ```bg_clr_feature```, ```bg_color_feature```, ```bg_clr_partners```, ```bg_clr_testimonsals```, ```section_background```, ```back```
* Button color keys: ```button_color```, ```button_bg_clr```, ```button_bg_color```, ```btn_background_color```; button text color: ```button_text_color```, ```buttonTextColor```, ```btn_text_color```, ```button_color_text```
* Other color keys: ```global_color```, ```color_icons```, ```logosBgColor```
* Style keys: ```product_style```, ```cat_style```, ```banner_type```, ```style_variant```, ```layout```
* Layout keys: ```container_type```, ```display_mode```, ```text_alignment```, ```position_title```, ```position_content```, ```background_position```, ```transition_effect```, ```overlay_opacity``` (0–100), ```min_height_mobile```, ```min_height_desktop```, ```border_color```, ```border_width```
* Items-per-row keys: ```number_on_sm``` (fallbacks: ```number_sm```, ```numberOnSm```, ```items_sm```, ```products_per_row```, ```products_per_row_mobile```, ```slides_visible_xs```, ```carousel_slides_xs```, ```grid_columns_xs```), ```number_on_md``` (```numberOnMd```, ```items_md```), ```number_on_lg``` (```numberOnLg```, ```items_lg```)
* Slider behavior keys: ```hide_dots```, ```show_dots```, ```hide_navs```, ```autoplay``` (fallbacks: ```autoplay_enabled```, ```auto_play```, ```auto_move```), ```autoplay_delay```
* Alignment keys: ```title_center``` boolean, or ```title_align```/```titleAlign```/```title_alignment```/```headings_align``` set to `"center"`
* Other behavior keys: ```show_as_column``` (fallbacks: ```show_column```, ```as_column```, ```is_vertical```), ```show_on_mobile```, ```hide_on_mobile```, ```show_button```, ```full_btn_border```, ```show_social``` (fallback: ```display_social_media```), ```controls```
* Section banner keys: ```section_banner``` (fallbacks: ```sectionBanner```, ```photo_back```), ```section_banner_link```/```sectionBannerLink```
* Side banner keys (products layouts): ```display_side_banner```, ```banner_show_mob```, ```banner_image```, ```banner_title```, ```banner_link```, ```banner_link_text```
* Sidebar keys (flat in settings): ```sideBar_title```, ```sideBar_desc```, ```sideBar_image```, ```sideBar_link```, ```sideBar_btn_text```, ```sideBar_text_color```, ```sideBar_desc_color```, ```options_design```
* Source category keys (what "view all" opens when a section lists one store category): ```category_id``` (fallbacks: ```categoryId```, ```category_uuid```), or the ```id``` of a ```productsCategory```/```products_category``` object — numeric ids only

**Boolean values**: section keys accept a real boolean, a number (`0` = false), or the strings `"true"`/`"1"` and `"false"`/`"0"`.

**Generic items list**: when a section carries a list under any of these keys, its objects are parsed as sub-items with the same key conventions above. The first key present wins, in this order: ```main_slider```, ```slider```, ```sliders```, ```slides```, ```frames```, ```hero_slider```, ```spicial_slider```, ```media_slides```, ```quick_links```, ```gallery```, ```twoimgrow```, ```threeimgrow```, ```items```, ```images```, ```ads```, ```banners```, ```banner_grid```, ```features```, ```features2```, ```store_features```, ```benefits```, ```partners```, ```store_partners```, ```brands_style_2```, ```testimonials```, ```testimonial```, ```reviews```, ```manual_reviews```, ```occasion_images```, ```tabs```, ```instagram```, ```posts```, ```infos```, ```catg_custom```, ```faqs_store_features```, ```faqs```, ```FAQs```, ```faq_items```, ```questions_cart```, ```questions```, ```brands``` (or ```brands.items```), ```list```, ```brand_list```, ```services```, ```stat_items```, ```stats```, ```feature_tab_items```, ```stagger_columns```, ```widgets_items```
* Three-tier banner lists ```top_banners``` + ```center_slides``` + ```bottom_banners``` are merged into one items list.
* Two-column hero lists ```slider_right``` + ```slider_left``` are merged into one slide list (hide either column with ```hide_first``` / ```hide_second```). When these keys are present, ```hide_element``` is ignored.

### Template names and settings shapes
* A namespaced template name is matched on the part after the last ```sections/``` — e.g. ```vitrin:sections/ai_generated.jinja``` resolves as ```ai_generated.jinja```.
* **Zid Sections Framework (fieldset keys)**: settings grouped as ```{group}_fieldset_{field}``` (e.g. ```content_fieldset_title```, ```layout_fieldset_products_per_row_mobile```) are read automatically. Each such key also answers to its bare name (```title```, ```products_per_row_mobile```), to ```component_content_{field}``` (content group) or ```component_control_{field}``` (every other group), and, for a ```_mobile```/```_desktop``` field, to the same names without the suffix (mobile wins). Explicit flat keys are never overwritten. In the ```buttons``` group, the short form (```buttons_fieldset_text_color```) gets only the ```component_control_*``` alias, so it cannot overwrite the section's own colors.
* An unmapped template that carries an items list **and** ```banners_per_row``` renders as a banners grid. Any other unmapped template is not rendered.

---

## 1. Slider Module
* Supported file names: ```main-slider.jinja```, ```main_slider2.jinja```, ```slider.jinja```, ```sslider.jinja```, ```img-slider.jinja```, ```templete-velvet-main-slider.jinja```, ```slider_img.jinja```, ```carousel.jinja```, ```cards-slider-section.jinja```, ```spicial-slider.jinja```, ```slider-imgs.jinja```, ```slide-sliderr.jinja```, ```hero-section.jinja```, ```media-slider.jinja```, ```slider-banners.jinja```, ```hero-media-swiper-showcase.jinja```, ```zahra-banners-showcase.jinja```, ```ai_generated.jinja```
* Supported slider items list keys: ```main_slider```, ```slider```, ```sliders```, ```slides```, ```frames```, ```hero_slider```, ```spicial_slider```, ```media_slides``` — or two columns ```slider_right``` + ```slider_left``` (hidden with ```hide_first``` / ```hide_second```), merged into one list
* Supported hide dots key: ```hide_dots``` boolean
* Supported autoplay keys: ```autoplay```, ```autoplay_enabled```, ```auto_play```, ```auto_move``` boolean (default: false); delay: ```autoplay_delay```
* Supported item type key: ```type```, ```slider_type``` — must be ```video``` or ```image``` (default: image); an item whose link points to a video file is also played as a video
* Supported item image keys: ```mobile_image```, ```image_mobile```, ```image```, ```img_slider_mobile```, ```img_slider```, ```background_image_mobile```, ```background_image_sm```, ```src_mobile```, ```background_image```, ```img_mobile```, ```image1```/```image2```, ```desktop```/```mobile```, ```desktop_poster```/```mobile_poster```, ```desktop_image```/```image_desktop```
* Supported item title keys: ```title```, ```heading```, ```image_title```
* Supported item subtitle keys: ```subtitle```, ```sub_title```, ```des```, ```desc```, ```description```, ```explain```
* Supported item badge text key: ```badge_text```, ```badge```, ```badge_label```
* Supported item overlay opacity key: ```overlay_opacity``` (number 0–100)
* Supported item text alignment key: ```text_alignment``` (start, center, end)
* Supported item button text keys: ```btn_text```, ```text_button```, ```button_text```, ```primary_button_text```, ```urlTitle```
* Supported item secondary button text key: ```secondary_button_text```
* Supported item secondary button url key: ```secondary_button_url```
* Supported item text color key: ```text_color```, ```textColor``` (default: white)
* Supported item button background color key: ```background_color```, ```button_color```, ```button_bg_clr``` (default: primary)
* Supported item button text color key: ```button_text_color```, ```buttonTextColor```
* Supported item link keys: ```url```, ```link```, ```href```, ```url_button```, ```video_link```, ```primary_button_url```, ```button_url```, ```cta_link```
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
* Supported file names: ```gallery.jinja```, ```ggallery.jinja```, ```template-velvet-gallery.jinja```, ```home-banners-section.jinja```, ```grid-images.jinja```, ```image-group.jinja```, ```two-pics.jinja```, ```features-gallery.jinja```, ```images-section.jinja```, ```banners-grid.jinja```, ```two-image-grid.jinja```, ```three-image-grid.jinja``` (3 columns by default)
* Supported gallery items list keys: ```gallery```, ```twoimgrow```, ```threeimgrow```, ```items```, ```images```, ```ads```, or the three tiers ```top_banners``` + ```center_slides``` + ```bottom_banners``` (merged)
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```sectionTitle```, ```heading```
* Supported grid layout keys: ```num_of_cols``` (columns), ```gap``` (spacing), ```border_radius```, ```custom_height```, ```enable_custom_height``` boolean
* Supported vertical layout key: ```show_as_column``` boolean (fallbacks: ```show_column```, ```as_column```, ```is_vertical```)
* Supported layout switches: ```viewStyle``` (```horizontal``` = scrolling row, ```vertical``` = stacked column), ```options_design``` (```horizantal```/```horizontal``` = scrolling row)
* Supported header keys: ```small_subtitle``` / ```small_subtitle_color``` (kicker), ```small_text``` / ```small_text_color``` (caption)
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
* Supported item shadow key: ```noshado``` boolean — true removes the tile shadow
* Supported item overlay keys (```features-gallery.jinja```): ```title```, ```count``` (line under the title), ```back``` (scrim color)

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
* Supported file names: ```features.jinja```, ```store-features.jinja```, ```features-section.jinja```, ```benefits.jinja```, ```features2.jinja```, ```feature-image-tabs.jinja```, ```stagger-showcase.jinja```, ```advantage-module.jinja```, ```feature-store.jinja```, ```benefits-row.jinja```
* Supported feature items list keys: ```features```, ```features2```, ```store_features```, ```benefits```, ```feature_tab_items```, ```stagger_columns```, ```widgets_items```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_section```, ```bg_clr_features```, ```background_color```, ```section_background``` (default: white)
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported main title color key: ```main_title_clr```
* Supported main description keys: ```des```, ```desc```, ```sub_title```, ```subtitle```, ```description```, ```section_description```
* Supported item image keys: ```image_mobile```, ```image```, ```img```, ```icon_image```, ```icon``` — ```icon``` may also be a keyword instead of an image URL, rendered as a built-in icon: ```shipping```/```delivery```/```truck```, ```payment```/```secure_payment```/```secure```/```security```, ```support```/```customer_service```/```service```, ```returns```/```refund```/```exchange```, ```quality```/```guarantee```/```warranty```, ```gift```, ```discount```/```offer```
* Supported item title keys: ```title```, ```text```
* Supported item description keys: ```des```, ```desc```, ```description```
* Supported item text color key: ```text_color``` (default: black)
* Supported feature title color key: ```title_feature_clr```, ```title_feature_color```
* Supported feature content color key: ```content_feature_clr```, ```content_feature_color```
* Supported feature individual bg color key: ```bg_clr_feature```, ```bg_color_feature```
* Supported title position key: ```position_title```, ```position_content```
* Supported container type key: ```container_type```
* Supported grid key: ```columns_mobile``` — renders the items as a wrapping grid with this many columns
* Supported icon style keys: ```featuresStyle_iconSize```, ```featuresStyle_iconColor```, ```featuresStyle_iconBgColor``` (fallback: ```icon_bg_color```)
* Supported text style keys: ```featuresStyle_textSize```, ```featuresStyle_textWeight```, ```featuresStyle_textColor``` (fallback: ```desc_color```) for the item description; ```featuresStyle_subtextSize```, ```featuresStyle_subtextWeight```, ```featuresStyle_subtextColor``` for the item title

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
* Supported file names: ```products.jinja```, ```offers.jinja```, ```products-section.jinja```, ```product_grid.jinja```, ```top_picks_products.jinja```, ```bestseller-section.jinja```, ```products-selected.jinja```, ```home-featured-products-section.jinja```, ```section_products.jinja```, ```home-columns-products.jinja```, ```custom_product.jinja```, ```fixed-products.jinja```, ```products-display-section.jinja```, ```featured-product-section.jinja```, ```spicial-products.jinja```, ```banner-with-products.jinja```, ```products-with-bg.jinja```, ```products-slider.jinja```, ```products-grid.jinja```, ```products-grid-hor.jinja```, ```video-with-products.jinja```, ```products-slider-small.jinja```, ```featured-product.jinja```, ```products-with-top-banner.jinja```, ```product-card.jinja```, ```curated-product-showcase.jinja```, ```product-tiles.jinja```, ```deals.jinja```, ```fresh-band.jinja```, ```bakery-band.jinja```
* Supported products block keys: ```products```, ```product``` (a single product object), ```products_category```, ```category```, ```results```, ```tab_products```, ```productsCategory```
* Supported products list keys inside the block: ```results```, ```products```, ```data```, ```items``` — each item may also be wrapped under ```products``` (Zid) or ```product``` (Unaizah Pro)
* Product references with no ```name```, ```price```, ```formatted_price```, ```sale_price``` or ```images``` (e.g. ```{"id": "…", "type": "product"}```) are skipped; a section left with no products is hidden
* Supported title keys: ```title```, ```title_offer```, ```section_title```, ```sectionTitle```, ```banner_title```, ```heading```
* Supported display key: ```display``` boolean (default: true)
* Supported display more keys: ```display_more``` boolean and its fallbacks (see Common Section Keys) — ```more_link```, ```view_all_url``` or a "more" label alone also enables it
* Supported more text keys: ```more_text```, ```loadMoreText```, ```load_more_text```, ```view_all_text```, ```see_all_text```, ```btn```; more url keys: ```btn_url```, ```more_url```, ```button_url```, ```more_link```, ```view_all_url```, ```see_all_url```
* Supported more text color key: ```more_clr```
* Supported url key: ```url```
* Supported module type key: ```module_type```
* Supported id key: ```id```
* Supported description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description``` — for ```fixed-products.jinja``` / ```spicial-products.jinja``` also ```small_text```, ```small_title```
* Supported description color key: ```desc_section_clr```, ```description_color```
* Supported title color keys: ```title_section_clr```, ```title_color```
* Supported background section color key: ```bg_section```
* Supported container type key: ```container_type```
* Supported layout key: ```viewStyle``` (fallbacks: ```display_mode```, ```layout```) — ```grid``` for a fixed grid; ```slider```, ```carousel```, ```horizontal``` or ```rail``` for a horizontal list
* Supported number per row key: ```number_on_sm``` (fallbacks: ```number_sm```, ```numberOnSm```, ```items_sm```, ```products_per_row```, ```products_per_row_mobile```, ```slides_visible_xs```, ```grid_columns_xs```), ```number_on_md```, ```number_on_lg```
* Supported hide dots key: ```hide_dots``` (setting it to ```false``` shows dots on horizontal lists)
* Supported title center key: ```title_center``` (or ```title_align: "center"```)
* Supported section banner keys: ```section_banner```/```sectionBanner```, ```section_banner_link```/```sectionBannerLink```
* Supported section banner display keys: ```showBannerImage``` boolean, ```bannerHeight```, ```bannerFit``` (a CSS ```object-fit``` value: ```cover```, ```contain```, ```fill```, ```none```, ```scale-down```); ```photo_back``` is a banner image shown below the grid
* Supported side banner keys: ```display_side_banner``` boolean, ```banner_image```, ```banner_title```, ```banner_link```, ```banner_link_text```, ```banner_show_mob```
* Supported video keys (```video-with-products.jinja```, ```products-with-top-banner.jinja```): ```video```, ```video_mobile```, ```top_banner_content_mobile_video```, ```top_banner_content_desktop_video```
* Supported countdown badge labels: ```ends_label```, ```starts_label```, ```current_label```, ```next_label``` — the badge counts down to the store-wide ```plus_offers_schedule``` setting (see Offers Clock Module)

> **Notes:**
> * ```products-section.jinja``` with no title and no ```small_subtitle```/```small_text```/```small_title``` is hidden entirely.
> * ```banner-with-products.jinja``` renders a media banner above a header-less grid; ```products-with-bg.jinja``` renders the grid over a full-bleed background image.
> * ```home-columns-products.jinja``` supports the multi-category ```nest``` list — each entry wraps its own ```products``` block and renders as an independent block.
> * ```fixed-products.jinja``` is always rendered as a fixed grid.
> * ```product-tiles.jinja```, ```fresh-band.jinja``` and ```bakery-band.jinja``` show their "shop all" link (```button_url``` / ```button_text```) inline in the header.

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
* Supported file names: ```category-products-section.jinja```, ```home-category-products.jinja```, ```home-products-section.jinja```, ```category-products.jinja```, ```featured-products-center.jinja```, ```Product-categories-section.jinja```
* Supported category module key: ```category``` — the section title and "view all" link are read from ```settings.category.name``` and ```settings.category.url```
* Supported category id key: ```id```
* Supported category name key: ```name```
* Supported products key: ```products```
* Supported display more key: ```display_more``` boolean (default: true)
* Supported more text keys: ```more_text```
* ```Product-categories-section.jinja``` also supports a promo banner: ```image```, ```title```, ```url```, and ```text``` as its button label

---

## 6. Categories Module
* Supported file names: ```category-section.jinja```, ```template-velvet-category-section.jinja```, ```home-categories.jinja```, ```categories.jinja```, ```categories_banner.jinja```, ```categories-selected.jinja```, ```home-categories-section.jinja```, ```categories-list.jinja```, ```category-list.jinja```, ```images-square.jinja```, ```category-style2.jinja```, ```category-style3.jinja```, ```categories-section.jinja```, ```categories-banner.jinja```, ```most-important-offers.jinja```, ```important-sections.jinja```, ```spicial-categories.jinja```, ```shop-by-category.jinja```, ```shop-by-price.jinja```, ```categories-grid.jinja```, ```featured-category.jinja```, ```new-collections.jinja```, ```category-tiles-showcase.jinja```, ```black-categories.jinja```, ```categories-02.jinja```, ```category-gallery.jinja```, ```category-chips.jinja```, ```categories-grid-section.jinja```
* Supported main title keys: ```title```, ```sectionTitle```, ```section_title```, ```banner_title```, ```heading```
* Supported subtitle keys: ```sectionSubTitle```, ```desc```
* Supported display more key: ```display_more``` boolean
* Supported more text keys: ```more_text```; more url keys: ```btn_url```, ```more_url```, ```more_link```
* Supported more text color key: ```more_clr```
* Supported categories items keys: ```categories```, ```categoriesList```, ```categories_list```, ```collection_list```, ```category_items```, ```category```, ```images_square```, ```category_style2```, ```spicial_categories```, ```prices```, ```tiles``` — each item may be wrapped under ```category```, ```selectedCategory```, or ```item```
* Supported wrapper keys next to a wrapped category: ```image```/```icon``` (tile icon), ```bg```/```cat_text_color``` (tile background)
* Items with no category id are still shown when they carry a name, image or ```url``` of their own (curated tiles link to their own ```url```); empty items left by deleted categories are dropped
* Supported "all categories" switch: ```categoriesType: "all_categories"``` lists the store's whole category tree instead of the section's items
* Supported card-style items key: ```category_style2``` (card layouts used by ```category-style2.jinja``` / ```category-style3.jinja```); ```featured-category.jinja``` uses the same card row with ```mcategories``` items (```url``` + ```custom_image```)
* Supported category style key: ```cat_style``` (fallbacks: ```product_style```, ```banner_type```, ```style_variant```) — values ```card_style2```, ```card_style3```, ```featured_box``` pick a card layout
* Supported container type key: ```container_type```
* Supported layout key: ```displayType``` (fallback: ```display_mode```) — ```grid```, or ```carousel```/```slider```
* Supported tile keys: ```tile_radius```, ```tile_title_position``` (```overlay``` or ```below```), ```tile_image_shape``` (```rounded```, ```square```/```sharp```), ```bg_card``` (card background)
* Supported grid tile keys (```categories-grid.jinja```): per item ```cta_text``` and ```product_count_label```; section-level ```default_cta``` (used when an item has no ```cta_text```)
* Supported number of items keys: ```number_on_sm``` (fallback: ```carousel_slides_xs```), ```number_on_md```, ```number_on_lg```
* Supported hide dots key: ```hide_dots```
* Supported hide navigation key: ```hide_navs```
* Supported title center key: ```title_center```
* Supported title color key: ```title_section_clr```
* Supported description color key: ```desc_section_clr```, ```description_color```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_section```

---

## 7. Categories with Products Module (Products Tabs)
* Supported file names: ```product-category.jinja```, ```home-tabs-section.jinja```, ```products_grid_tabs.jinja```, ```products-tab.jinja```, ```tabs-products.jinja```, ```multi-products.jinja```, ```products-grid-tabs.jinja```, ```categories-tabs.jinja```, ```tabbed-products-showcase.jinja```
* Supported tabs list keys: ```products_categories```, ```product_tabs```, ```tab_products```, ```categories```, ```tabs```, ```products``` (for ```categories```, ```tabs``` and ```products```, entries must look like tabs)
* Each tab supports: ```category``` object (with ```id```, ```name```/```label```, ```url```, ```products```/```results```), ```label``` (overrides the category name as the tab text), ```display_more``` boolean, ```more_url```, ```more_text```, ```max``` (cap on rendered products; 0 = no cap)
* Alternative tab shape: ```tab_title``` (or ```tab_label```) + ```tab_products``` (products payload with ```url```)
* Alternative inline shape: ```title``` (or ```name```) + ```products: { "results": [...] }```
* Alternative numbered shape: ```tab_1_title``` + ```tab_1_category``` (category object) or ```tab_1_products``` (product list), up to ```tab_10_*```
* Alternative multi-box shape (```multi-products.jinja```): ```box1_name```/```box1_products``` up to ```box10_name```/```box10_products``` — each ```boxN_products``` holds ```results```
* Unaizah Pro tab shape: ```title``` + ```listProducts``` (`category` or `selected`) + ```productsCategory``` object or inline ```products``` list (items wrapped under ```product```)
* Supported main title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported title color key: ```title_color```
* Supported caption keys: ```small_text```, ```small_text_color```
* Supported more text color key: ```more_clr```
* Supported tab colors: ```tab_active_bg_color```, ```tab_active_text_color```, ```tab_inactive_bg_color```, ```tab_inactive_text_color```
* Supported tab alignment key: ```tabs_align``` (```start```/```left```, ```center```, ```end```/```right```)
* Supported layout key: ```viewStyle``` (fallback: ```display_mode```) — ```grid```, or ```slider```/```carousel```
* Supported per-tab default limit: ```tab_products_default_limit```
* Supported banner keys: ```showBannerImage```, ```bannerHeight```, ```bannerFit``` (a CSS ```object-fit``` value)

> **Note:** If the category ```id``` is missing, it is extracted automatically from the category ```url``` (e.g. ```/categories/1415209/...```).

---

## 8. Instagram Module
* Supported file names: ```instagram-gallery.jinja```, ```instagram.jinja```, ```black-instagram-feed.jinja```
* Supported main title key: ```title```
* Supported instagram username key: ```instagram_account```
* Supported images list keys: ```instagram```, ```images``` or ```posts``` — every object must contain ```image``` and ```url```

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
* Supported file names: ```banner.jinja```, ```large-banner.jinja```, ```big-banner.jinja```, ```image-with-text.jinja```, ```banner_img.jinja```, ```hero.jinja```, ```banner-image.jinja```, ```banner-text.jinja```, ```banner-grid.jinja```, ```banners.jinja```, ```ad_image.jinja```, ```mini-banner.jinja```, ```banars-sections.jinja```, ```deal-days.jinja```, ```banner-2.jinja```, ```news-banar.jinja```, ```services.jinja```, ```image-text.jinja```, ```black-image-text.jinja```, ```banner-section.jinja```, ```national-day-hero.jinja```, ```photo-banner.jinja```, ```split-banner.jinja```, ```home-section.jinja```
* ```branches.jinja``` is also rendered as a single banner when it carries no ```locations```/```branches``` list (a promo tile with ```image```, ```title```, ```sub_title```, ```desc```, ```url```)
* Supported image keys: ```mobile_image```, ```image_mobile```, ```mobimage```, ```img_mobile```, ```image```, ```img_banner```, ```image_desktop```/```desktop_image```, ```image1```/```image2```, ```background_image_mobile```, ```background_image```
* Supported background image key: ```background_banner```, ```backgroundimage```
* Supported link keys: ```url```, ```link```, ```banner_link```, ```button_url```
* Supported background color keys: ```color```, ```background_color```, ```bg_color``` (default: white)
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading```
* Supported subtitle keys: ```subtitle```, ```sub_title```, ```des```, ```desc```, ```description```, ```section_description```, ```paragraph```
* Supported second paragraph keys: ```description_02```, ```desc_02```, ```description2```, ```sub_description```
* Supported badge text key: ```badge_text```, ```badge```, ```badge_label```, ```slogan```
* Supported extra overlay lines: ```mark_text```, ```note_text```
* Supported overlay opacity key: ```overlay_opacity``` (0–100)
* Supported text color keys: ```text_color```, ```textColor```, ```textcolor``` (default: white); body text color: ```texts_color```
* Supported button visibility key: ```show_button``` boolean (default: true)
* Supported button text keys: ```button_text```, ```btn_text```, ```primary_button_text```, ```urlTitle```, ```url_title_1```
* Supported secondary button keys: ```secondary_button_text```, ```secondary_button_url``` (shown beside the primary button)
* Supported button text color keys: ```button_text_color```, ```btn_text_color```, ```button_color_text``` (default: white)
* Supported button bg color keys: ```button_bg_color```, ```button_color```, ```btn_background_color``` (default: primary)
* Supported container type key: ```container_type```

**Multi-image layouts:**
* ```banners.jinja``` — a wrap grid of images. Grid keys: ```banners``` (items list), ```banners_per_row```, ```banners_per_row_mobile```, ```stack_banners_mobile``` boolean
* ```banner-grid.jinja``` — one large banner followed by a row of smaller banners (items under ```banner_grid```), each with gradient, title and CTA
* ```services.jinja``` — a list of promo tiles under ```services``` (each ```image```, ```url```, ```urlTitle```)
* ```split-banner.jinja``` — image beside the content: ```image_position``` (```start``` or ```end```), ```tone``` (```dark``` default, or ```light```)
* Any unmapped section that carries an items list **and** the ```banners_per_row``` key is automatically rendered as a banners grid

> **Note:** in ```banners.jinja``` the ```items``` list wins over ```images```/```ads```/```banners```, so a stale ```banners``` array does not replace the merchant's slides.

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
* Supported file names: ```home-brands-section.jinja```, ```home-brands.jinja```, ```brands.jinja```, ```brands-style-2.jinja```, ```brands-section.jinja```
* Supported brand list keys: ```brands``` (a plain list, or an object ```{ "title", "display", "items": [...] }```), ```brands_style_2```, ```list```, ```brand_list```
* Supported title keys: ```title```, ```banner_title```, ```section_title```, ```heading``` (or ```brands.title```)
* Supported kicker key (above the title): ```small_subtitle```, ```SubTitle```
* Supported caption key (below the title): ```small_text```
* Supported brand item image keys: ```image```, ```img```, ```logo```
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
* Supported file names: ```home-faqs-section.jinja```, ```home-faqs.jinja```, ```faq.jinja```, ```faqs.jinja```, ```yasmeen-faqs.jinja```, ```faq-section.jinja```, ```common-questions.jinja```
* Supported FAQs list keys: ```faqs_store_features```, ```faqs```, ```FAQs```, ```faq_items```, ```questions_cart```, ```questions```
* Supported item question keys: ```title```, ```question```, ```faq```
* Supported item answer keys: ```answer```, ```content```, ```text```, ```description```
* Supported store FAQs key: ```showStoreFaqs``` boolean — when true, the store's global FAQ list is shown instead of the section's own items
* Supported background color key: ```details_bg``` (default: white)
* Supported video image key: ```details_video_img```
* Supported video url key: ```details_video``` (YouTube URL)
* Supported title key: ```details_title```
* Supported description key: ```details_desc```
* Supported header keys: ```small_subtitle``` (kicker above the title), ```small_text``` (caption below it)
* Supported item style keys: ```qColor```, ```qSize```, ```qWeight```, ```qBgColor``` (question); ```aColor```, ```aSize```, ```aWeight``` (answer); ```titleAlign```
* Supported open-first key: ```openFirst``` (fallback: ```expand_first```) — opens the first question

---

## 13. Testimonials Module
* Supported file names: ```testimonials.jinja```, ```home-reviews-section.jinja```, ```home-testimonials-section.jinja```, ```review-slider.jinja```, ```reviews.jinja```, ```customer-reviews-section.jinja```
* Supported testimonials list keys: ```testimonials```, ```testimonial```, ```reviews```, ```manual_reviews```
* Supported main title keys: ```title```, ```title_offer```, ```sectionTitle```, ```section_title```, ```banner_title```, ```heading```
* Supported main description keys: ```des```, ```desc```, ```sub_title```, ```description```, ```section_description```
* Supported main title color key: ```main_title_clr```
* Supported title position key: ```position_title```, ```position_content```
* Supported background color keys: ```bg_color```, ```bg_clr```, ```bg_clr_testimonsals```, ```background_color```, ```section_background```
* Supported hide dots key: ```hide_dots```
* Supported item name keys: ```author```, ```customerName```, ```customer_name```, ```client_name```, ```reviewer_name```, ```name```
* Supported item image keys: ```client_image```, ```image```
* Supported item date key: ```date```
* Supported item review text keys: ```text```, ```review```, ```reviews```, ```review_text```, ```content```, ```customerReview```, ```client_opinion```, ```comment```, ```des```
* Supported item rating keys: ```rating```, ```stars_count```, ```stars``` (numeric, displayed as stars)
* Supported style keys: ```stars_color```, ```comma_color```; layout: ```viewStyle``` (```grid```, or ```slider```/```carousel```)
* Supported product reviews source: ```reviews_method: true``` with a ```product``` object, or ```productReviews_active: true``` with a ```productReviews_product``` object — the section then shows that product's real reviews; hide parts with ```productReviews_hideDate```, ```productReviews_hideName```, ```productReviews_hideRating```

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
* Supported video url keys: ```video```, ```video_upload```; a mobile-specific source (played instead when present): ```video_mobile```, ```mobile_video```
* Supported rotating words key: ```dynamic_words``` — a list of ```{ "word": "..." }``` (or plain strings) typed one after another beside the title
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
* Supported countdown image keys: ```countdownImage``` (list of objects with ```image```), ```image```, ```background_image_mobile```, ```background_image```, ```background_image_sm```, or an ```occasion_images``` list
* Supported occasion toggle key: ```occasion_enable```
* Supported title/description/badge keys: ```title```, ```description```, ```badge_text``` (common fallbacks apply)
* Supported button keys: ```btn_text```, ```btn_url``` (falls back to ```url```)
* Supported expired text key: ```message_expired``` (fallbacks: ```expired_message```, ```messageExpired```) — shown instead of the timer once the date has passed

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
* Supported slider list: ```announcement_bar_slider``` (rows of ```text``` + ```url```, rotated one message at a time; one ```text``` may hold several messages separated by ```|```)
* Supported link key: ```announcement_bar_url```
* Supported background color keys: ```announcement_bar_background_color```, ```announcement_bar_BackgroundColor```, ```news_bg```, ```announcement_bar_BgColor```, ```scroll_announcement_bar_background_color```
* Supported text color keys: ```announcement_bar_text_color```, ```announcement_bar_TextColor```, ```news_text```, ```scroll_announcement_bar_text_color``` (falls back to the first ```announcement_bar_advertisement_bar``` item's ```text_color```)
* Supported font size keys: ```announcement_bar_TextFontSize```, ```announcement_bar_text_font_size```
* Supported behavior keys: ```announcement_bar_move```, ```announcement_bar_stop_move```, ```announcement_bar_text_marquee```, ```announcement_bar_enable_animation```, ```announcement_bar_pause_on_hover```, ```announcement_bar_animation_speed```, ```announcement_bar_autoplaySpeed```/```announcement_bar_autoplay_speed```, ```announcement_bar_page_display``` (fallback: ```scroll_announcement_bar_page_display```)
* **Moving strip** (```moved_announcement_*```): used when ```moved_announcement_display``` is on and ```announcement_bar_display``` is not. Keys: ```moved_announcement_bgColor```, ```moved_announcement_textColor```, ```moved_announcement_page_display```, ```moved_announcement_announcements```; it scrolls when ```moved_announcement_textMove``` is on or ```moved_announcement_moveAnimation``` is ```marquee```
* **Scroll strip** (```scroll_announcement_bar_*```): when ```scroll_announcement_bar_display``` is on and ```scroll_announcement_bar_text_list``` (items with ```text```, optional ```url```) is not empty, it replaces the plain bar and scrolls every message as one marquee; the first item ```url``` is the strip's link
* On/off strings accepted for the moving and scroll strips: ```true```, ```"1"```, ```"true"```, ```"on"```, ```"yes"```

---

## 20. Advertisement Bar Module
* Supported file names: ```advertisement-bar.jinja```, ```home-news-section.jinja```, ```ticker-wrap.jinja```, ```black-moving-text.jinja``` (rendered as an image + text marquee strip)
* Supported visibility key: ```hide_element``` boolean
* Supported items list keys: ```advertisement_bar```, ```news```, ```store_news``` — or, with no list, the flat strings ```text``` and ```text_2```
* Supported item image keys: ```image```, ```img```
* Supported item title keys: ```title```, ```name```, ```text```
* Supported item url keys: ```url```, ```link```, ```href```
* Supported item text color key: ```text_color``` (the section-level ```text_color``` applies to items without one)
* Supported background color keys: ```background_color```, ```text_bg```
* Supported marquee speed keys: ```marquee_speed```, ```speed```
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
* Supported file names: ```branches.jinja```, ```home-store-locations.jinja```
* Supported branches list keys: ```branches```, ```locations``` (a ```branches.jinja``` with neither list is rendered as a banner — see Banner Module)
* Supported item keys: ```name``` (fallback: ```title```), ```address```, ```phone```, ```working_hours```
* Supported item map keys: ```map_url``` (a ready map link, preferred), or coordinates ```location_lat```/```latitude``` + ```location_lng```/```longitude```; ```map``` (an embed ```<iframe>```) is shown as an inline map
* Supported main title key: ```title```; colors: ```title_color```, ```small_subtitle_color```, ```small_text_color```

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
* Supported file names: ```video-stories.jinja```, ```videos-story.jinja```, ```products-video-slider.jinja```
* Supported items list key: ```videos``` — each item contains ```video``` (URL), optional ```poster``` image, and an optional ```product``` object (also accepted as a full product object under ```product_id```)
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
* Supported file names: ```home-blog.jinja```, ```blogs.jinja```, ```blog.jinja```, ```custom-slider.jinja```, ```blog-cards.jinja```
* Supported blogs list keys: ```blog```, ```blogs```, ```store_custom```, ```articles```
* Supported main title key: ```title```; kicker: ```small_subtitle```
* Supported item image keys: ```image```, ```img```
* Supported item title keys: ```topic```, ```title```, ```text``` — when ```topic``` is set, ```title``` is shown as the author line
* Supported item author key: ```author```
* Supported item excerpt keys: ```Paragraph```, ```paragraph```, ```description```, ```desc```, ```excerpt```
* Supported item date badge keys: ```date``` (e.g. year), ```dated``` (e.g. day and month)
* Supported item url keys: ```url```, ```link```, ```href```
* Supported item button text keys: ```btn_text```, ```key```, ```read_more_label```

---

## 29. Points Products Module
* Supported file names: ```points-products.jinja```
* The section is recognized by the app but is intentionally not rendered inside the home screen (loyalty points products are handled by the app's native loyalty module).

---

## 30. Banner Tabs Module
* Supported file names: ```banner-tabs.jinja```
* Supported tabs list key: ```tabs``` — each item's ```title``` is the tab label; tapping a tab swaps the content shown below it
* Supported item keys: ```image``` (common image keys apply), ```description```, ```btn_text```/```urlTitle``` (button label), ```url```

---

## 31. Media Banner Module
* Supported file names: ```media-banner.jinja``` (poster only), ```media-text-banner.jinja``` (poster + heading text + buttons)
* Supported media keys: ```component_content_media_type```, ```component_content_video```, ```component_content_mobile_video```, ```component_content_desktop_poster```, ```component_content_mobile_poster```
* Supported buttons key: ```component_content_buttons``` — a list of ```{ "button_title", "button_link" }```
* Supported control keys: ```component_control_autoplay```, ```component_control_hide_controls```, ```component_control_media_full_height```, ```component_control_corner_radius```, ```component_control_title_size```, ```component_control_subtitle_size```, ```component_control_description_size```, ```component_control_text_weight```, ```component_control_buttons_size```, ```component_control_buttons_variant```
* Supported color keys: ```text_color```, ```buttons_background_color```, ```buttons_text_color```
* Title and description use the common keys. Fieldset-style settings (```content_fieldset_*```, ```layout_fieldset_*```, …) are mapped onto these names automatically — see *Template names and settings shapes*.

---

## 32. Flash Sale Module
* Supported file names: ```flash-sale.jinja```
* Supported product key: ```product``` — a single product object
* Supported end date key: ```sale_end_date``` (read as UTC)
* Supported button label key: ```cta_text```
* Supported style keys: ```background_color```, ```text_color```, ```text_size```, ```textAlign```, ```timer_background_color```, ```timer_text_color```, ```timer_labels_color```, ```buttons_background_color```, ```buttons_text_color```, ```buttons_size```, ```buttons_variant```

---

## 33. Coupon Module
* Supported file names: ```coupon.jinja```
* Supported code keys: ```coupon_text```, ```coupon```, ```code```, ```coupon_code```
* Supported tile image keys: ```icon```, then the common image keys
* Supported text keys: title and subtitle use the common title/description keys; copy-button label uses the common button text keys
* Supported style keys: ```title_color```, ```title_fontSize```, ```title_fontWeight```, ```subtitle_color```, ```subtitle_fontSize```, ```subtitle_fontWeight```, ```coupon_color```, ```coupon_fontSize```, ```coupon_fontWeight```, ```couponBgColor```, ```button_color```, ```button_bgColor```, ```button_fontSize```, ```button_fontWeight```
* Supported spacing keys: ```topSpace```, ```bottomSpace```

---

## 34. Auto Products Module
* Supported file names: ```auto-products.jinja```
* The section carries no products of its own; the app fetches them from the store using the section's query:
  * Sort key: ```products``` in the form ```"<field>|<asc|desc>"``` (e.g. ```"created_at|desc"```), or an explicit ```ordering```
  * Price range: ```filterPrice_from```, ```filterPrice_to```
  * Discounted only: ```discountedOnly``` boolean
  * Restrict to categories: ```category_id``` (or ```categories``` for several)
  * Hand-picked products: ```product_ids``` (wins over every other filter)
  * Hide sold-out products: ```hide_out_of_stock``` boolean
* The fetched list is rendered with the Products Module layout and keys.

---

## 35. Offers Module
* Supported file names: ```offer-section.jinja```
* Supported products block keys: same as the Products Module
* Supported title key: common title keys
* Supported background color: common background color keys
* Supported card switches: ```nordus``` boolean (square cards with no border), ```books``` boolean (no tinted plate behind the product image)

---

## 36. Category Cards Module
* Supported file names: ```category-video.jinja```
* Supported items list key: ```catg_custom``` — each item: ```title```, ```description```, ```image```, ```url```
* Supported per-item colors: ```background``` (card), ```bacolor``` (button background), ```baclors``` (button text)
* Supported per-item button label: ```tit1```

---

## 37. Categories Nav Module
* Supported file names: ```categories-nav.jinja```
* Supported items list key: ```categories_nav``` — each item: ```title``` (required), ```url```

---

## 38. Counter Up Module
* Supported file names: ```counter-up.jinja```, ```stats-numbers.jinja```, ```statistics.jinja```
* Supported items list keys: any generic items key, e.g. ```items```, ```stat_items```, ```stats```
* Supported item value keys: ```number_item```, ```number```, ```count```, ```value```
* Supported item label keys: common title keys (including ```label```) and description keys
* Supported color keys: ```background_color```/```bg_color```, ```title_color```, ```text_color```, ```description_color```, ```number_color```/```value_color```, ```card_background_color```, ```card_border_color```

---

## 39. Contact Us Module
* Supported file names: ```contact-us.jinja```
* Supported contact keys: ```contact_us_text```, ```contact_us_email```, ```contact_us_phone```, ```contact_us_address```, ```contact_us_map```
* Supported header keys: common title keys, ```small_subtitle``` (kicker), ```small_text``` (caption)
* Supported color keys: ```title_color```, ```small_subtitle_color```, ```small_text_color```

---

## 40. Paragraph Module
* Supported file names: ```paragraph.jinja```, ```promo-band.jinja```
* A centered heading block with no image: common title and description keys
* ```promo-band.jinja``` also renders a single link as a button: ```url``` + ```link_text```
* Supported style keys: ```text_color``` (applies to every text), ```background_color```, ```text_align```, ```text_size```

---

## 41. Spacer Module
* Supported file names: ```spacer.jinja```
* Supported height keys: ```mobileHeight``` (fallback: ```height```)
* Supported style keys: ```background_color```, ```use_container``` boolean (adds side padding)

---

## 42. Feature Steps Module
* Supported file names: ```black-image-features.jinja``` (numbered titles beside an image), ```sense-pyrmid-fragrance.jinja``` (numbered cards with a description)
* Supported steps key: ```features_list``` — one step per line; each line is ```title``` or ```title | description```
* Supported image key: common image keys
* Supported color keys: ```text_color```, ```feature_title_color```, ```feature_text_color```, ```feature_number_color```, ```feature_bg_color```

---

## 43. Branches Map Module
* Supported file names: ```branches-map.jinja```
* Supported regions key: ```regions``` — each region: ```name``` + ```cities``` list of ```{ "label", "maps_url" }```; regions are shown as tabs, cities as a second row of tabs
* Supported flat list key (used when there are no regions): ```branches``` — each item: ```label```, ```maps_url``` (or ```map_iframe```, an embed ```<iframe>```)
* Supported keys: common title keys, ```subtitle```, ```visit_text``` (link label)

---

## 44. Reels Module
* Supported file names: ```reels-section.jinja```
* Supported items list key: ```videos``` — each item: ```url``` (a TikTok page link, opened externally), ```poster```, optional ```product``` object
* Supported spacing keys: ```topSpace```, ```bottomSpace```

---

## 45. Shoppable Image Module
* Supported file names: ```interactive-image-section.jinja```
* Supported image keys: common image keys (```desktop_image```/```mobile_image``` …); aspect ratio: ```image_ratio_mobile``` (percentage, 100 = square)
* Supported hotspots key: ```hotspots``` — each item: ```product``` object, ```x_position_mobile```, ```y_position_mobile``` (percent of the image)
* Supported color keys: ```dot_color```, ```dot_icon_color```, ```price_color```, ```background_color```
* Supported spacing keys: ```topSpace```, ```bottomSpace```

---

## 46. Hero Canopy Module
* Supported file names: ```hero-canopy.jinja```
* Supported text keys: ```heading``` (or common title keys), ```badge```, ```highlight```
* Supported greeting keys: ```greeting_morning```, ```greeting_evening```, ```show_greeting``` (false hides it), ```show_hijri``` (false hides the Hijri date)
* Supported tiles key: ```tiles``` — each tile: ```icon```, ```title```, ```text```, ```url```
* Supported featured product keys: a products block (Products Module keys) + ```products_pick``` (```discount``` = the product with the highest discount)
* Supported button keys: ```button_text``` (primary — always opens the products list sorted by popularity), ```button2_text``` + ```button2_url``` (secondary)
* Supported color keys: ```title_color```, ```text_color```

---

## 47. Offers Clock Module
* Supported file names: ```offers-clock.jinja```
* Counts down to the store-wide ```plus_offers_schedule``` setting (see Global Settings)
* Supported label keys: ```ends_label```, ```starts_label```, ```current_label```, ```next_label```
* Supported "no offer" keys: ```none_title```, ```none_text```
* Supported button keys: ```shop_text```, ```shop_url```, ```remind_text``` (adds the next window to the calendar)
* Supported header keys: common title keys, ```small_subtitle```; colors: ```title_color```, ```small_subtitle_color```

---

## 48. Bento Module
* Supported file names: ```bento.jinja```
* Supported items: generic items list — each item: ```title```, ```description```, ```image```, ```url```, ```tag```, ```link_text```, ```size``` (```big``` for a large tile)
* Supported header keys: common title and description keys; colors: ```title_color```, ```small_text_color```

---

## 49. Magazine Module
* Supported file names: ```magazine.jinja```
* Supported pages key: ```pages``` — each page: ```image``` (thumbnail), ```full``` (full-size image)
* Supported keys: ```pdf_url```, ```pdf_text``` (button label), ```valid_text```, ```autoplay``` boolean, ```interval``` (seconds)
* Supported header keys: common title keys, ```small_subtitle```; colors: ```title_color```, ```small_subtitle_color```

---

## 50. Baskets Module
* Supported file names: ```baskets.jinja```
* Supported baskets key: ```baskets``` — each basket: ```title```, ```subtitle```, ```badge```, ```image```, ```items``` (one item per line), ```color``` (accent), ```season``` (```always```, or ```ramadan``` = shown only during Ramadan)
* Supported header keys: common title keys, ```small_subtitle```; colors: ```title_color```, ```small_subtitle_color```

---

## 51. Live Band Module
* Supported file names: ```live-band.jinja```
* Supported keys: ```video_url```, ```poster```, ```badge_text```, ```offline_title```, ```schedule_text```
* Supported live window keys: ```live_from```, ```live_to``` (```HH:mm```), ```always_live``` boolean — outside the window the offline panel is shown
* Supported header keys: common title keys, ```small_subtitle```; colors: ```title_color```, ```small_subtitle_color```

---

## 52. Journey Module
* Supported file names: ```journey.jinja```
* Supported stops key: ```stops``` — each stop: ```city```, ```note```, ```year```
* Supported "next stop" keys: ```next_year```, ```next_text```, ```next_note```
* Supported header keys: common title keys, ```small_subtitle```; colors: ```title_color```, ```small_subtitle_color```

---

## 53. Feedback Module
* Supported file names: ```feedback.jinja```
* Supported feedback types key: ```types``` — options separated by ```|```
* Supported keys: common title, description and button text keys, ```small_subtitle```; colors: ```title_color```, ```small_subtitle_color```

---

## 54. Reorder Module
* Supported file names: ```reorder.jinja```
* Shows the signed-in customer's most recent order with a one-tap reorder; hidden for guests
* Supported keys: common title keys, ```small_subtitle```, ```all_text``` (label of the "all orders" link); colors: ```title_color```, ```small_subtitle_color```

> **Not rendered:** ```usuals.jinja``` (its content lives only in the shopper's browser storage, so the home response carries no data for it).

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

Each link item supports: ```title```/```name```/```text```, ```url```/```link```/```href```, ```image```/```img```, ```icon```.

Groups 1–4 also accept the camelCase shape: ```links_links1Title```, ```links_links1List```, and ```links_links1Show``` (the inverse of ```links_1_hide```).

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

### Offers Schedule
| Key | Usage |
|---|---|
| ```plus_offers_schedule``` | A recurring weekly deals window, sent as one string of five fields separated by ```\|```: name, recurrence, start day + time, end day + time, shop url — e.g. ```عروض التطبيق \| أسبوعي \| الأربعاء 06:00 \| السبت 23:59 \| /categories/…```. Day names must be Arabic weekday names, times are ```HH:mm```, the recurrence must be ```أسبوعي``` (weekly — the only one supported), and the shop url is optional. It lives at the root of the home response's ```settings``` (next to ```components```), and drives the Offers Clock Module and the countdown badge on products sections. |

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
