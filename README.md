# **Theming websites** - overiding with css

css are styling elements of a html page, allmost all websites have fancy elements which are results of this.

websites are themed by defining custom css and making them override the original.

2 commons ways to do this,
* using plugins or addons
* defining in userContent.css

# **Using Plugins** - [stylish](https://github.com/stylish-userstyles/stylish), [stylus](https://github.com/openstyles/stylus)

* finding styles and applying on the fly with inline check

![inline_find](../master/screenshots/stylish/inline_find.png)

* user freedom to customize styles (depends on the creator), css in this repo allows user to choose 3 colors (foreground, background
and outline) stylish plugin replaces syntax `/*[[color]]*/` with appropirate label [[more](https://userstyles.org/help/coding#help-style-settings)]

![choosing color](../master/screenshots/stylish/customize.png)

# **Defining in userContent.css** (specific for firefox)

[[guide](https://www.reddit.com/r/FirefoxCSS/comments/73dvty/tutorial_how_to_create_and_livedebug_userchromecss/)] 
along with chrome/userChrome.css (not necessary for this particular purpose) create a file chrome/userContent.css

when variables are defined in userContent.css it effects globally
```
:root {
    --background: #000000;
    --foreground: #b7e0b6;
    --outline: #809c7f;
}
```
instead of explicitly choosing colors for each website styles, using variables like ` background: var(--background) !important; ` in 
all styles will use colors defined in userContent.css (uniform theme among different websites)

css in styles plugin along with appropriate namespace eg: ` @-moz-document domain("duckduckgo.com") ` can be copied to userContent.css directly so external plugin is no longer needed.

# Screenshots
(images will redirect to userstyles.org)

[![physicsforums](../master/screenshots/pf/pf_1.png)](https://userstyles.org/styles/183180/physicsforums-custom-back-foregrounds-outline)

[![duckduckgo](../master/screenshots/ddg/Screenshot_2020-05-03-fomalhaut-at-DuckDuckGo.png)](https://userstyles.org/styles/183178/duckduckgo-minimal-custom-back-fore-grounds)


## Notes

* when using 'inspect element' try to find inherited parts so effects are throughout instead of defining in ` this element {..} ` unless that's what you're intended.
* good intro about css [noob-friendly guide](https://developer.mozilla.org/en-US/docs/Web/CSS) from mozilla


   [![license](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
