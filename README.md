Google Font Optimization Tests
==============================

Testing the following font inclusion methods over simulated 3G in Chrome Dev tools, and Google Page Speed Insights

- Merriweather:
  - 400,
  - 300,
  - 300italic,
  - 700,
  - 400italic,
  - 700italic,
  - 900,
  - 900italic
- Montserrat:
  - 400,
  - 700
- RobotoCondensed:
  - 700

# @Import Method
  - [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Fimport-method.html&tab=desktop)
  - Mobile Page Speed Results: 71/100
  - Desktop Page Speed Results: 89/100
  - Requests: 11
  - Transferred: 108KB
  - Finish 1.8s
  - DOM Content Loaded: 201ms
  - Load: 313ms

# Link Method
  - [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Flink-method.html&tab=mobile)
  - Mobile Page Speed Results: 75/100
  - Desktop Page Speed Results: 91/100
  - Requests: 11
  - Transferred: 108KB
  - Finish 1.69s
  - DOM Content Loaded: 210ms
  - Load: 319ms


# Font API Method
  - [Link To Page Speed Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fsomecallmejosh.github.io%2Fgoogle-font-tests%2Fjavascript-method.html&tab=desktop)
  - Mobile Page Speed Results: 100/100
  - Desktop Page Speed Results: 100/100
  - Requests: 14
  - Transferred: 138KB
  - Finish 2.3s
  - DOM Content Loaded: 227ms
  - Load: 654ms
