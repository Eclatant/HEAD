# HEAD
당신의 문서에 있는 `<head>` 안에 들어갈 수 있는 모든 것의 목록

## 목차

- [최소한의 권장 사항](#recommended-minimum)
- [Elements](#elements)
- [Meta](#meta)
  - [Meta: 권장하지 않음](#meta-not-recommended)
- [Link](#link)
  - [Link: 권장하지 않음](#link-not-recommended)
  - [Favicons](#favicons)
- [Social](#social)
  - [Facebook / Open Graph](#facebook--open-graph)
  - [Facebook / Instant Articles](#facebook--instant-articles)
  - [Twitter](#twitter)
  - [Google+ / Schema.org](#google--schemaorg)
  - [OEmbed](#oembed)
- [Browsers / Platforms](#browsers--platforms)
  - [Apple iOS](#apple-ios)
  - [Apple Safari](#apple-safari)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
  - [Microsoft Internet Explorer: Legacy, Do Not Use!](#microsoft-internet-explorer-legacy-do-not-use)
- [Browsers (Chinese)](#browsers-chinese)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [App Links](#app-links)
- [Notes](#notes)
  - [Performance](#performance)
- [Other Resources](#other-resources)
- [Related Projects](#related-projects)
- [Other Formats](#other-formats)
- [Translations](#translations)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

<!-- ## Recommended Minimum -->
## 최소한의 권장 사항 <a name="recommended-minimum"></a>

<!-- Below are the essential tags for basic, minimalist websites: -->
다음은 기본적인 웹 사이트의 필수 태그에 대한 최소 사항입니다.

```html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!-- 위의 3 가지 메타 태그는 *반드시* head 내에 먼저 있어야합니다. 다른 head 내용은 이 태그 *뒤에* 와야합니다. -->
<title>Page Title</title>
```

## Elements

``` html
<!-- 문서 제목 -->
<title>Page Title</title>

<!-- 문서 내에 포함 된 모든 상대 URL에 사용될 기본 URL -->
<base href="https://example.com/page.html">

<!-- 외부 CSS -->
<link rel="stylesheet" href="styles.css">

<!-- 내부 CSS -->
<style>
  /* ... */
</style>

<!-- JavaScript -->
<script src="script.js"></script>
<noscript><!--no JS alternative--></noscript>
```

## Meta

``` html
<meta charset="utf-8"> <!-- set character encoding for the document -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!-- 위의 3 가지 메타 태그는 *반드시* head 내에 먼저 있어야합니다. 다른 head 내용은 이 태그 *뒤에* 와야합니다. -->

<!-- 리소스가 로드되는 위치를 제어할 수 있습니다. -->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">
<!-- 가능한 한 문서의 초기에 배치하십시오. -->
<!-- 이 태그 아래의 컨텐츠에만 적용됩니다. -->

<!-- 웹 응용 프로그램의 이름 (웹 사이트가 응용 프로그램으로 사용되는 경우에만 사용해야 함.) -->
<meta name="application-name" content="Application Name">

<!-- 페이지에 대한 간단한 설명 (최대 150 자) -->
<!-- *일부 상황*에서는 이 설명이 검색 결과에 표시된 스니펫의 일부로 사용됩니다. -->
<meta name="description" content="A description of the page">

<!-- 검색 엔진 크롤링 및 색인 생성 동작 제어 -->
<meta name="robots" content="index,follow,noodp"><!-- All Search Engines -->
<meta name="googlebot" content="index,follow"><!-- Google Specific -->

<!-- Google에 '사이트 링크 검색 창 표시 안함'을 알림 -->
<meta name="google" content="nositelinkssearchbox">

<!-- 이 페이지에 대한 번역을 제공하지 않도록 Google에 알립니다. -->
<meta name="google" content="notranslate">

<!-- Google Search Console의 소유권 확인 -->
<meta name="google-site-verification" content="verification_token">

<!-- 웹 사이트 구축에 사용 된 소프트웨어의 이름을 짓는 데 사용됩니다. (예 : WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- 사이트 주제에 대한 간략한 설명 -->
<meta name="subject" content="your website's subject">

<!-- 매우 짧은 (10 단어 이하) 설명. 주로 학술 논문 용 -->
<meta name="abstract" content="">

<!-- 전체 도메인 이름 또는 웹 주소 -->
<meta name="url" content="https://example.com/">

<meta name="directory" content="submission">

<!-- 사이트 콘텐츠를 기준으로 일반 연령 등급 부여 -->
<meta name="rating" content="General">

<!-- 리퍼러(referrer) 정보 전달 방법을 제어 할 수 있습니다. -->
<meta name="referrer" content="no-referrer">

<!-- 가능한 전화 번호의 자동 감지 및 형식을 사용하지 않도록 설정합니다. -->
<meta name="format-detection" content="telephone=no">

<!-- 'off'로 설정하여 DNS 프리 패치를 완전히 선택 해제합니다. -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- 클라이언트 식별을 위해 클라이언트 웹 브라우저에 쿠키를 저장합니다. -->
<meta http-equiv="set-cookie" content="name=value; expires=date; path=url">

<!-- 특정 프레임에 표시 할 페이지를 지정합니다. -->
<meta http-equiv="Window-Target" content="_value">

<!-- Geo tags -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- 국가 코드 (ISO 3166-1): 필수, 주(state) 코드 (ISO 3166-2): 선택; eg. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- eg. content="New York City" -->
```

- [Meta tags that Google understands](https://support.google.com/webmasters/answer/79812?hl=en)
- [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- [ICBM on Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- [Geotagging on Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

<!-- ### Meta: Not Recommended -->
### Meta: 권장하지 않음 <a name="meta-not-recommended"></a>
다음은 채택률이 낮거나 권장되지 않는 메타 속성입니다.

```html
<!-- 문서 언어를 선언하는 데 사용되지만 잘 지원되지는 않습니다. <html lang="">를 사용하는 것이 더 낫습니다. -->
<meta name="language" content="en">

<!-- Google은 Bing을 스팸의 지표로 간주합니다. -->
<meta name="keywords" content="your,keywords,here,comma,separated,no,spaces">
<!-- 어떤 검색엔진이든 사용하지 않습니다. -->
<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm">

<!-- 스팸 봇이 이메일 주소를 쉽게 수집 할 수있는 방법 제공합니다. -->
<meta name="reply-to" content="email@example.com">

<!-- <link rel = "author"> 또는 humans.txt 파일을 사용하는 것이 더 좋습니다. -->
<meta name="author" content="name, email@example.com">
<meta name="designer" content="">
<meta name="owner" content="">

<!-- 검색 봇에게 일정 기간 후에 페이지를 다시 방문하도록 지시합니다. 대부분의 검색 엔진이 웹 페이지를 다시 크롤링 할 때 임의의 간격을 사용하기 때문에 이 기능은 도움이 되지 않습니다. -->
<meta name="revisit-after" content="7 days">

<!-- 일정 시간이 지나면 사용자를 새 URL로 보냅니다. -->
<!-- W3C는 이 태그를 사용하지 않을 것을 권하며, 대신 서버 측에서 301 리디렉션을 사용하는 것을 권합니다. -->
<meta http-equiv="refresh" content="300; url=https://example.com/">

<!-- 웹 사이트의 주제를 설명합니다. -->
<meta name="topic" content="">

<!-- 웹 사이트의 회사 또는 목적에 대한 간략한 요약 -->
<meta name="summary" content="">

<!-- keywords 메타 태그와 기능이 동일하여 사용되지 않는 태그 -->
<meta name="classification" content="business">

<!-- URL과 같은 기능입니다. 오래 되었으며, 지원되지 않습니다. -->
<meta name="identifier-URL" content="https://example.com/">

<!-- keywords 태그와 유사한 기능 -->
<meta name="category" content="">

<!-- 웹 사이트가 모든 국가 및 언어로 표시되는지 확인합니다. -->
<meta name="coverage" content="Worldwide">

<!-- coverage 태그와 동일합니다. -->
<meta name="distribution" content="Global">

<!-- 인터넷에서 어떤 사용자가 액세스 할 수 있는지 제어합니다. -->
<meta http-equiv="Pics-label" content="value">

<!-- 케시 컨트롤 -->
<!-- 케시 컨트롤은 서버사이드에서 컨트롤하는 것이 더 낫습니다.  -->
<meta http-equiv="Expires" content="0">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Cache-Control" content="no-cache">
```

## Links

``` html
<!-- 중복되는 콘텐츠 문제들을 방지합니다. -->
<link rel="canonical" href="https://example.com/2010/06/9-things-to-do-before-entering-social-media.html">

<!-- 이전에는 아이콘 링크 앞에 포함되었지만 더 이상 사용되지 않습니다. -->
<link rel="shortlink" href="https://example.com/?p=42">

<!-- 현재 문서의 AMP HTML 버전에 대한 링크 -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- CSS 스타일 시트를 가리킨다. -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- 웹 응용 프로그램과 관련된 정보를 담고있는 JSON 파일에 대한 링크 -->
<link rel="manifest" href="manifest.json">

<!-- 문서 작성자에 대한 링크 -->
<link rel="author" href="humans.txt">

<!-- 링크 컨텍스트에 적용되는 저작권 선언문을 나타냅니다. -->
<link rel="copyright" href="copyright.html">

<!-- 문서가 다른 언어를 통해 컨텐츠를 제공할 시 다른 언어로 된 문서의 위치에 대한 참조를 제공합니다. -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- 저자 또는 다른 사람에 대한 정보 제공 -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- 현재 문서에 대한 아카이브 링크가 포함 된 문서의 링크를 제공합니다. -->
<link rel="archives" href="https://example.com/2003/05/" title="May 2003">

<!-- 계층 구조에서 최상위 리소스에 대한 링크 -->
<link rel="index" href="https://example.com/" title="DeWitt Clinton">

<!-- 문서의 시작점을 지정합니다. -->
<link rel="start" href="https://example.com/photos/pattern_recognition_1_about/" title="Pattern Recognition 1">

<!-- 현재 문서가 위치해있는 시퀀스의 이전 리소스로 연결됩니다. -->
<link rel="prev" href="https://example.com/opensearch/opensearch-and-openid-a-sure-way-to-get-my-attention/" title="OpenSearch and OpenID? A sure way to get my attention.">

<!-- 자체 참조 제공 - 문서에서 여러 참조가 있는 경우 유용합니다. -->
<link rel="self" type="application/atom+xml" href="https://example.com/atomFeed.php?page=3">

<!-- 일련의 문서를 정의 (첫 번째, 다음, 이전 및 마지막 문서) -->
<link rel="first" href="https://example.com/atomFeed.php">
<link rel="next" href="https://example.com/atomFeed.php?page=4">
<link rel="previous" href="https://example.com/atomFeed.php?page=2">
<link rel="last" href="https://example.com/atomFeed.php?page=147">

<!-- 타사 서비스를 사용하여 블로그를 관리 할 때 사용됩니다. -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- 다른 WordPress 블로그가 귀하의 WordPress 블로그 또는 게시물에 링크되면 자동으로 주석을 사용합니다. -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- 사이트에서 링크 할 때 URL에 알립니다. -->
<link rel="webmention" href="https://example.com/webmention">

<!-- 외부 HTML 파일을 현재 HTML 파일에서 로드합니다. -->
<link rel="import" href="component.html">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds(구독) -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
```

### Link: 권장하지 않음 <a name="link-not-recommended"></a>
다음은 사용을 권장하지 않는 링크와 관련된 내용입니다. :

```html
<link rel="shortcut icon" href="path/to/favicon.ico">

<!-- 유용하지 않으며 버그가 있습니다. 여기를 참조하세요. https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/Y_2eFRh9BOs/gULYapoRBwAJ -->
<link rel="subresource" href="styles.css">
```

### Favicons

``` html
<!-- IE 10 이하 -->
<!-- 링크가 없으면 favicon.ico 라는 파일을 루트 디렉토리에 두십시오. -->

<!-- IE 11, Chrome, Firefox, Safari, Opera의 경우 -->
<link rel="icon" href="path/to/favicon-16.png" sizes="16x16" type="image/png">
<link rel="icon" href="path/to/favicon-32.png" sizes="32x32" type="image/png">
<link rel="icon" href="path/to/favicon-48.png" sizes="48x48" type="image/png">
<link rel="icon" href="path/to/favicon-62.png" sizes="62x62" type="image/png">
<link rel="icon" href="path/to/favicon-192.png" sizes="192x192" type="image/png">
<!-- 자세한 내용: https://bitsofco.de/all-about-favicons-and-touch-icons/ -->
```

- [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)

## Social

### Facebook / Open Graph

``` html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
<!-- Facebook: https://developers.facebook.com/docs/sharing/webmasters#markup -->
<!-- Open Graph: http://ogp.me/ -->
```

- [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- [Open Graph protocol](http://ogp.me/)

### Facebook / Instant Articles

``` html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- 아티클의 웹 버전 URL -->
<link rel="canonical" href="http://example.com/article.html">

<!-- 이 아티클에 사용할 스타일 -->
<meta property="fb:article_style" content="myarticlestyle">
```

- [Facebook Instant Articles: Creating Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- [Instant Articles: Format Reference](https://developers.facebook.com/docs/instant-articles/reference)

### Twitter

``` html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<!-- 자세한 내용: https://dev.twitter.com/cards/getting-started -->
<!-- Validate: https://dev.twitter.com/docs/cards/validation/validator -->
```

- [Twitter Cards: Getting Started Guide](https://dev.twitter.com/cards/getting-started)
- [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Google+ / Schema.org

``` html
<link href="https://plus.google.com/+YourPage" rel="publisher">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

### Pinterest

여기에 따르면 [to their help center](https://help.pinterest.com/en/articles/prevent-people-saving-things-pinterest-your-site) Pinterest는 사람들이 당신의 웹 사이트에서 정보를 저장하지 못하게 합니다. `description`은 선택 사항입니다.

``` html
<meta name="pinterest" content="nopin" description="Sorry, you can't save from my website!">
```

### OEmbed

``` html
<link rel="alternate" type="application/json+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- [oEmbed format](http://oembed.com/)

## Browsers / Platforms

### Apple iOS

``` html
<!-- 스마트 앱 배너 -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- 가능한 전화 번호의 자동 감지 및 형식을 사용하지 않도록 설정합니다. -->
<meta name="format-detection" content="telephone=no">

<!-- 홈 스크린에 추가합니다. -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- 터치 아이콘 -->
<link rel="apple-touch-icon" href="path/to/apple-touch-icon.png">
<link rel="apple-touch-icon-precomposed" href="path/to/apple-touch-icon-precomposed.png">
<!-- iOS 8+ no longer support precomposed, only apple-touch-icon is required -->

<!-- 대부분의 경우, `head`에 있는 180x180x 크기의 터치 아이콘 하나로 충분합니다. -->
<!-- 당신이 유일한 아이콘을 원한다면 다른 아이콘 크기를 활용하십시오. -->
<!-- 디바이스에 의해 결정됩니다. -->
<link rel="apple-touch-icon" sizes="57x57" href="path/to/icon@57.png">
<link rel="apple-touch-icon" sizes="72x72" href="path/to/icon@72.png">
<link rel="apple-touch-icon" sizes="114x114" href="path/to/icon@114.png">
<link rel="apple-touch-icon" sizes="144x144" href="path/to/icon@144.png">

<!-- Startup Image ( 더 이상 사용되지 않음 ) -->
<link rel="apple-touch-startup-image" href="path/to/startup.png">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- [Apple Meta Tags](https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

### Apple Safari

```html
<!-- Pinned Site -->
<link rel="mask-icon" href="path/to/icon.svg" color="red">
```

### Google Android

``` html
<meta name="theme-color" content="#E64545">

<!-- 홈 스크린에 추가합니다. -->
<meta name="mobile-web-app-capable" content="yes">
<!-- 자세한 내용: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

``` html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- 번역 프롬프트 사용 중지 -->
<meta name="google" value="notranslate">
```
### Google Chrome Mobile (Android Only)

Chrome 31 이후로 웹 앱을 Safari와 같은 '앱 모드'로 설정할 수 있습니다.

``` html
<!-- `manifest`에 연결하고 `manifest` 메타 데이터를 정의합니다. -->
<!-- manifest.json의 예는 아래 링크에서 찾을 수 있습니다. -->
<link rel="manifest" href="manifest.json">

<!-- 웹 페이지를 웹 앱으로 정의하십시오. -->
<meta name="mobile-web-app-capable" content="yes">

<!-- 첫 번째 공식 권장 형식입니다.  -->
<link rel="icon" sizes="192x192" href="nice-highres.png">
<link rel="icon" sizes="128x128" href="niceicon.png">
<!-- Apple 접두어가 붙은 형식은 더 이상 사용되지 않습니다. -->
<link rel="apple-touch-icon" sizes="128x128" href="niceicon.png">
<link rel="apple-touch-icon-precomposed" sizes="128x128" href="niceicon.png">
```

[Google Developer](https://developer.chrome.com/multidevice/android/installtohomescreen)

### Microsoft Internet Explorer

``` html
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta http-equiv="cleartype" content="on">
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Windows Phone에서 IE 10의 링크 강조 표시 비활성화 (https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) -->
<meta name="msapplication-tap-highlight" content="no">

<!-- Pinned sites (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Contoso Pinned Site Caption">
<meta name="msapplication-tooltip" content="Example Tooltip Text">
<meta name="msapplication-starturl" content="/">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">

<meta name="msapplication-allowDomainApiCalls" content="true">
<meta name="msapplication-allowDomainMetaTags" content="true">
<meta name="msapplication-badge" content="frequency=30; polling-uri=http://example.com/id45453245/polling.xml">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile">
<meta name="msapplication-square150x150logo" content="path/to/logo.png">
<meta name="msapplication-square310x310logo" content="path/to/largelogo.png">
<meta name="msapplication-square70x70logo" content="path/to/tinylogo.png">
<meta name="msapplication-wide310x150logo" content="path/to/widelogo.png">
<meta name="msapplication-task" content="name=Check Order Status;action-uri=./orderStatus.aspx?src=IE9;icon-uri=./favicon.ico">
<meta name="msapplication-task-separator" content="1">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="path/to/tileimage.jpg">
<meta name="msapplication-window" content="width=1024;height=768">
```

### Microsoft Internet Explorer: Legacy, 절대 사용하지 마세요!

``` html
<!-- IE 6에서 이미지 위로 마우스를 가져 가면 이미지 툴바를 비활성화. (https://msdn.microsoft.com/en-us/library/ms532986(v=vs.85).aspx) -->
<meta http-equiv="imagetoolbar" content="no">

<!-- 입력 / 단추를 구성하기 위해 Windows 테마 사용 안 함 (https://support.microsoft.com/en-us/kb/322240) -->
<meta name="MSThemeCompatible" content="no">

<!-- IE 6 베타에서만 등장한 기능을 사용 중지합니다. (https://stackoverflow.com/q/2167301) -->
<meta name="MSSmartTagsPreventParsing" content="true">

<!-- 페이지 간 전환 (https://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx) -->
<meta http-equiv="Page-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Page-Exit" content="revealtrans(duration=3,transition=12)">
<meta http-equiv="Site-Enter" content="revealtrans(duration=2,transition=2)">
<meta http-equiv="Site-Exit" content="revealtrans(duration=3,transition=12)">
```

## App Links

``` html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">
<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">
<!-- Web Fallback -->
<meta property="al:web:url" content="http://applinks.org/documentation">
<!-- 자세한 내용: http://applinks.org/documentation/ -->
```

- [App Links Docs](http://applinks.org/documentation/)

## Browsers (Chinese)

### 360 Browser

``` html
<!-- 렌더링 엔진을 순서대로 선택 -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

``` html
<!-- 화면을 지정된 방향으로 잠급니다. -->
<meta name="x5-orientation" content="landscape/portrait">
<!-- 이 페이지를 전체 화면으로 보여줍니다. -->
<meta name="x5-fullscreen" content="true">
<!-- 페이지가 "응용 프로그램 모드"로 표시됩니다. (전체 화면 등) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

``` html
<!-- 화면을 지정된 방향으로 잠급니다. -->
<meta name="screen-orientation" content="landscape/portrait">
<!-- 이 페이지를 전체 화면으로 보여줍니다. -->
<meta name="full-screen" content="yes">
<!-- '텍스트 모드'인 경우에도 UC 브라우저는 이미지를 표시합니다. -->
<meta name="imagemode" content="force">
<!-- 페이지가 "응용 프로그램 모드"로 표시됩니다. (전체 화면, 제스처 금지 등) -->
<meta name="browsermode" content="application">
<!-- 이 페이지에서 UC 브라우저의 "야간 모드"를 비활성화합니다. -->
<meta name="nightmode" content="disable">
<!-- 데이터 전송을 줄이기 위해 페이지를 단순화합니다. -->
<meta name="layoutmode" content="fitscreen">
<!-- UC 브라우저의 "이 페이지에 단어가 많은 경우 글꼴 크기 조정"기능을 비활성화합니다. -->
<meta name="wap-font-scale" content="no">
```

- [UC Browser Docs](http://www.uc.cn/download/UCBrowser_U3_API.doc)

## Notes

### Performance
<!-- Moving the `href` attribute to the beginning of an element improves compression when GZIP is enabled, because the `href` attribute is used in `a`, `base` and `link` tags. -->
`href` 속성을 요소의 시작 부분으로 옮기면 GZIP이 활성화되었을 때 압축이 향상됩니다. (`href` 속성이 `a`,`base` 와 `link` 태그에서 사용될 때)

Example:

``` html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">
```

## Other Resources

- [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

## Related Projects

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - `HEAD` 스니펫을 위한 Atom 패키지
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - `HEAD` 스니펫을 위한 Sublime Text 패키지
- [head-it](https://github.com/hemanth/head-it) - `HEAD` 스니펫을 위한  CLI 인터페이스
- [vue-head](https://github.com/ktquez/vue-head) - Vue.js에 대한`HEAD` 태그의 메타 정보 조작

## Other Formats

- [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

## Translations

- [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- [Italian](https://github.com/Fakkio/HEAD)
- [Japanese](http://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- [Russian/Русский](https://github.com/Konfuze/HEAD)
- [Turkish/Türkçe](https://github.com/mkg0/HEAD)
- [Korean](https://github.com/lutece/HEAD)

## Contributing

Open an issue or a pull request to suggest changes or additions.

Please follow these steps for pull requests:

- Modify only one tag, or one related set of tags at a time
- Use double quotes on attributes
- Don't include a trailing slash in self-closing elements — the HTML5 spec says they're optional
- Consider including a link to documentation that supports your change

### Contributors

Check out all the super awesome [contributors](https://github.com/joshbuchea/HEAD/graphs/contributors).

## Author

**[Josh Buchea](http://joshbuchea.com/)**

## License

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Josh Buchea](http://joshbuchea.com) has waived all copyright and related or neighboring rights to this work.
