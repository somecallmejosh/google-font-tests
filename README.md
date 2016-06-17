Google Font Optimization Tests
==============================

Testing the following font inclusion methods over simulated 3G in Chrome Dev tools, and Google Page Speed Insights

#Option 1 - All Variants From Google CDN

Robot is only using one variant, because a project I'm working on only requires Roboto Condensed Bold (700);

- Merriweather:
  - 400,
  - 300,
  - 300italic,
  - 700,
  - 400italic,
  - 700italic,
  - 900,
  - 900italic
- Merriweather Fallback:
  - `font-family: Georgia, Times, "Times New Roman", serif;`
- Montserrat:
  - 400,
  - 700
- Montserrat Fallback:
  - `font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;`
- RobotoCondensed:
  - 700
- RobotoCondensed Fallback:
  - `font-family: "Arial Black", "Arial Bold", Gadget, sans-serif;`

## @Import Method
  - [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Fimport-method.html&tab=desktop)
  - Mobile Page Speed Results: 71/100
  - Desktop Page Speed Results: 89/100
  - Requests: 11
  - Transferred: 108KB
  - Finish 1.8s
  - DOM Content Loaded: 201ms
  - Load: 313ms

## Link Method
  - [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Flink-method.html&tab=mobile)
  - Mobile Page Speed Results: 75/100
  - Desktop Page Speed Results: 91/100
  - Requests: 11
  - Transferred: 108KB
  - Finish 1.69s
  - DOM Content Loaded: 210ms
  - Load: 319ms

## Javascript Method
  - [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Fjavascript-method.html&tab=desktop)
  - Mobile Page Speed Results: 100/100
  - Desktop Page Speed Results: 100/100
  - Requests: 14
  - Transferred: 138KB
  - Finish 2.3s
  - DOM Content Loaded: 227ms
  - Load: 654ms

## All Variants Assessment

Expected to see faster load times on Javascript method. Seems to load much faster due to the font fallbacks, but it's actually a heavier payload with longer load times. Still, the javascript option is likely the ideal solution out of the 3 options above.

#Option 2 - Normal Variants From Google CDN. Bold, italics variants Generated Synthetically (by the browser)

- Merriweather:
  - 400
- Montserrat:
  - 400
- Roboto Condensed
  - 700

Using the same fallbacks from above.

## @import Method
- [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Fnormal-variants%2Fimport-method.html&tab=mobile)
- Mobile Page Speed Results: 71/100
- Desktop Page Speed Results: 89/100
- Requests: 5
- Transferred: 33.7KB
- Finish 846ms
- DOM Content Loaded: 204ms
- Load: 300ms

## Link Method
- [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Fnormal-variants%2Flink-method.html)
- Mobile Page Speed Results: 75/100
- Desktop Page Speed Results: 91/100
- Requests: 5
- Transferred: 33.4KB
- Finish 803ms
- DOM Content Loaded: 213ms
- Load: 305ms

## Javascript Method
- [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Fnormal-variants%2Fjavascript-method.html&tab=desktop)
- Mobile Page Speed Results: 100/100
- Desktop Page Speed Results: 100/100
- Requests: 6
- Transferred: 40.2KB
- Finish 1.06s
- DOM Content Loaded: 205ms
- Load: 536ms


## Normal Variants Assessment

Doesn't seem to offer huge performance gains over the full stack variants originally tested.
