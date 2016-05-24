# Codepen Embeds

## Pick the Shortcode

We are working closely to the original embed-code given by the Codepen Website thus editors won't have to worry too much about syntax and also won't have to type much themselves.

![image](https://cloud.githubusercontent.com/assets/3417446/7510141/627bfc7e-f499-11e4-865c-a1218ff7b6b3.png)

### Shortcode

Shortcode: `[codepen_embed %settings% caption="{text}"] {text} [/codepen_embed]`

Additionally we added the Shortcode for automatically adding a caption to a Codepen embed (see above).

### Settings ###

In case someone wanted to customize the way the embed is displayed inside the article, we can sure have that (whereas we haven't been using it so far at all).

| Attribute | Default | Note
|---|---|---|
| theme_id |  - | 0
| slug_hash | - | Required
| user |  - |    Not required
| default_tab |  result |  html/css/js/result
| height |    300 |  Not a part of themes
| show_tab_bar | true | true/false, PRO only
| animations |   run |  run/stop-after-5
| border | none | none/thin/thick
| border_color | #000000 | Hex Color Code
| tab_bar_color    | #3d3d3e | Hex Color Code
| tab_link_color   | #76daff | Hex Color Code
| active_tab_color | #cccccc | Hex Color Code
| active_link_color| #000000 | Hex Color Code
| link_logo_color  | #ffffff | Hex Color Code
| custom_css_url |   - |    URL to CSS-File
