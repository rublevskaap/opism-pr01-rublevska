# Практична робота № 1

**Дисципліна:** Основи побудови інформаційних систем та мереж

**Тема:** Спостереження за процесом звернення до вебресурсу. Побудова власної моделі рівнів взаємодії

| | |
|---|---|
| **Прізвище, ім'я** |Рублевська Поліна |
| **Група** |F5 2.02 |
| **Номер варіанта** |23 |
| **Домен варіанта** |alpinelinux.org |
| **Середовище виконання** | macOS |
| **Версія curl** |curl 8.7.1 (x86_64-apple-darwin25.0) |
| **Дата виконання** |20.09.2026 |

---

## Частина A. Збір експериментальних даних

### A.1. Запит із діагностичним виводом

**Команда:**

```
curl -v https://alpinelinux.org
```

**Вивід:**

```
* Host alpinelinux.org:443 was resolved.
* IPv6: (none)
* IPv4: 213.219.36.190
*   Trying 213.219.36.190:443...
* Connected to alpinelinux.org (213.219.36.190) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* (304) (IN), TLS handshake, Unknown (8):
* (304) (IN), TLS handshake, Certificate (11):
* (304) (IN), TLS handshake, CERT verify (15):
* (304) (IN), TLS handshake, Finished (20):
* (304) (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / AEAD-AES256-GCM-SHA384 / [blank] / UNDEF
* ALPN: server accepted h2
* Server certificate:
*  subject: CN=alpinelinux.org
*  start date: Aug  1 02:01:46 2026 GMT
*  expire date: Oct 30 02:01:45 2026 GMT
*  subjectAltName: host "alpinelinux.org" matched cert's "alpinelinux.org"
*  issuer: C=US; O=Let's Encrypt; CN=YR2
*  SSL certificate verify ok.
* using HTTP/2
* [HTTP/2] [1] OPENED stream for https://alpinelinux.org/
* [HTTP/2] [1] [:method: GET]
* [HTTP/2] [1] [:scheme: https]
* [HTTP/2] [1] [:authority: alpinelinux.org]
* [HTTP/2] [1] [:path: /]
* [HTTP/2] [1] [user-agent: curl/8.7.1]
* [HTTP/2] [1] [accept: */*]
> GET / HTTP/2
> Host: alpinelinux.org
> User-Agent: curl/8.7.1
> Accept: */*
> 
* Request completely sent off
< HTTP/2 200 
< server: nginx
< date: Sun, 20 Sep 2026 19:05:35 GMT
< content-type: text/html
< content-length: 9143
< last-modified: Sun, 20 Sep 2026 17:26:11 GMT
< etag: "6ab01733-23b7"
< accept-ranges: bytes
< strict-transport-security: max-age=31536000
< x-frame-options: DENY
< x-content-type-options: nosniff
< 
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="description" content="Alpine Linux">
        <title>index | Alpine Linux</title>

        <link rel="stylesheet" href="/css/pure-min.css" />
        <link rel="stylesheet" href="/css/grids-responsive-min.css" />
        <link rel="stylesheet" href="/css/fontawesome.min.css" />
        <link rel="stylesheet" href="/css/fa-solid.min.css" />
        <link rel="stylesheet" href="/css/fa-brands.min.css" />
        <link rel="stylesheet" href="/css/fa-v4-shims.min.css" />
        <link rel="stylesheet" href="/css/styles.css" />
        <link rel="shortcut icon" href="/alpine-logo.ico" />
        <link rel="me" href="https://fosstodon.org/@alpinelinux" />
        <link rel="alternate" type="application/atom+xml" href="/atom.xml" />
    </head>
    <body>
        <div id="wrapper">
            <header class="pure-g" id="header">
                <div class="pure-u-1 pure-u-lg-4-24">
                    <div class="logo">
                        <a href="/"><img src="/alpinelinux-logo.svg" class="pure-img" alt="" /></a>
                    </div>
                </div>
                <input type="checkbox" id="menu-toggle-cb">
                <label id="menu-toggle" for="menu-toggle-cb" onclick><s class="bar"></s><s class="bar"></s><s class="bar"></s></label>
                <div class="pure-u-1 pure-u-lg-20-24 box-relative menu-wrapper">
                    <nav class="pure-menu pure-menu-horizontal menu-local">
                        <ul class="pure-menu-list">
                            <li class="pure-menu-item"><a href="/about/" class="pure-menu-link">About</a></li>
                            <li class="pure-menu-item"><a href="/downloads/" class="pure-menu-link">Downloads</a></li>
                            <li class="pure-menu-item"><a href="/releases/" class="pure-menu-link">Releases</a></li>
                            <li class="pure-menu-item"><a href="/community/" class="pure-menu-link">Community</a></li>
                            <li class="pure-menu-item"><a href="/sponsors/" class="pure-menu-link">Sponsors</a></li>
							<li class="pure-menu-item"><a href="/donate/" class="pure-menu-link">Donate</a></li>
                        </ul>
                    </nav>
                    <nav class="pure-menu pure-menu-horizontal menu-external">
                        <ul class="pure-menu-list">
                            <li class="pure-menu-item"><a href="https://docs.alpinelinux.org" class="pure-menu-link">docs</a></li>
                            <li class="pure-menu-item"><a href="https://wiki.alpinelinux.org" class="pure-menu-link">wiki</a></li>
                            <li class="pure-menu-item"><a href="https://gitlab.alpinelinux.org" class="pure-menu-link">git</a></li>
                            <li class="pure-menu-item"><a href="https://gitlab.alpinelinux.org/alpine/aports/-/issues" class="pure-menu-link">issues</a></li>
                            <li class="pure-menu-item"><a href="https://pkgs.alpinelinux.org" class="pure-menu-link">packages</a></li>
                            <li class="pure-menu-item"><a href="https://mirrors.alpinelinux.org" class="pure-menu-link">mirrors</a></li>
                            <li class="pure-menu-item"><a href="https://security.alpinelinux.org" class="pure-menu-link">security</a></li>
                        </ul>
                    </nav>
                </div>
            </header>
            <div class="banner">
                <div class="banner-content">
                    <h1>Small. Simple. Secure.</h1>
                    <h3>Alpine Linux is a security-oriented, lightweight Linux distribution based on musl libc and busybox.</h3>
                </div>
            </div>
            <div id="content" class="index">
                <div class="pagedate">
                    <time datetime=""></time>
                </div>
                <div class="pure-g">
   
    <div class="pure-u-1 pure-u-md-1-2">
        <div class="l-box">
            <h2>
                <a href="/atom.xml" class="atom"><i class="fa fa-rss"></i></a>
                Alpine News
            </h2>
            <ul class="home-list">
                <li><time>2026-09-17</time>  <a href="posts/Alpine-3.21.8-3.22.6-3.23.6-3.24.2-released.html">Alpine 3.21.8, 3.22.6, 3.23.6 and 3.24.2 released</a></li>
                <li><time>2026-06-21</time>  <a href="posts/Alpine-3.22.5-3.23.5-released.html">Alpine 3.22.5, 3.23.5 released</a></li>
                <li><time>2026-06-13</time>  <a href="posts/Alpine-3.24.1-released.html">Alpine 3.24.1 released</a></li>
                <li><time>2026-06-09</time>  <a href="posts/Alpine-3.24.0-released.html">Alpine 3.24.0 released</a></li>
                <li><time>2026-04-15</time>  <a href="posts/Alpine-3.20.10-3.21.7-3.22.4-3.23.4-released.html">Alpine Linux stable releases 3.20.10, 3.21.7, 3.22.4, 3.23.4</a></li>
                <li><time>2026-01-27</time>  <a href="posts/Alpine-3.20.9-3.21.6-3.22.3-3.23.3-released.html">Alpine 3.20.9, 3.21.6, 3.22.3 and 3.23.3 released</a></li>
                <li><time>2026-01-18</time>  <a href="posts/2026-01-18-new-sponsors-strenghten-infrastructure.html">Follow-Up: New Sponsors Strengthen Alpine Linux’s Infrastructure and CI Ecosystem</a></li>
                <li><time>2025-12-17</time>  <a href="posts/Alpine-3.23.2-released.html">Alpine 3.23.2 released</a></li>
                <li><time>2025-12-03</time>  <a href="posts/Alpine-3.23.0-released.html">Alpine 3.23.0 released</a></li>
                <li><time>2025-10-08</time>  <a href="posts/Alpine-3.19.9-3.20.8-3.21.5-3.22.2-released.html">Alpine 3.19.9, 3.20.8, 3.21.5 and 3.22.2 released</a></li>
            </ul>
            <a class="pure-button read-more" href="/posts">Read more</a>
        </div>

    </div>

    <div class="pure-u-1 pure-u-md-1-2">
        <div class="l-box">
            <h2>
                <a href="https://gitlab.alpinelinux.org/alpine/aports" class="cgit">
                    <i class="fa fa-git "></i>
                </a>
                Latest development
            </h2>
            <ul class="home-list">
                <li><time datetime="2026-09-20T17:09:43+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=547fef411dbd4239eef917af7a06655b32a4a539">testing&#x2F;py3-b2sdk: upgrade to 2.13.0</a></li>
                <li><time datetime="2026-09-20T16:54:49+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=5b6a890af2680a8c747f62dde33610becf8ca415">community&#x2F;plattenalbum: upgrade to 2.7.0</a></li>
                <li><time datetime="2026-09-20T15:19:33+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=6a66fd842d71c97eb61b2405d02ac6dd1d26cf67">community&#x2F;leocad: upgrade to 26.09</a></li>
                <li><time datetime="2026-09-20T15:11:09+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=42139a6d98390d31276a9b2ae6075c95683f0218">community&#x2F;breezy: add options=net, add lockfile</a></li>
                <li><time datetime="2026-09-20T14:54:06+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=68e052af6f59085ed3d685c3393260fb9cdf326d">community&#x2F;pv: upgrade to 1.12.0 and take over maintainership</a></li>
                <li><time datetime="2026-09-20T14:20:30+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=8b45e998db776de69f0b85b63a340c20c4e8754d">community&#x2F;thin-provisioning-tools: upgrade to 1.3.4</a></li>
                <li><time datetime="2026-09-20T13:43:47+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=a21473e2e011394a5a600256541d5a5db0d5116e">community&#x2F;kirigami-addons: upgrade to 1.14.1</a></li>
                <li><time datetime="2026-09-20T12:48:12+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=b56db466bcf2dc06d9bd3efed7fd256ca4de58c3">community&#x2F;farbfeld: drop maintainership</a></li>
                <li><time datetime="2026-09-20T12:45:12+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=ffa4e23d92431a9ceecdbc8807474920352fca0e">community&#x2F;ghex: upgrade to 50.4</a></li>
                <li><time datetime="2026-09-20T11:15:44+00:00">2026-09-20</time>  <a href="http://git.alpinelinux.org/aports/commit/?id=50928543cc6c279a900ebfb31924617ecb848eed">testing&#x2F;py3-slidge-style-parser: upgrade to 0.3.0</a></li>
            </ul>
            <a class="pure-button read-more" href="https://gitlab.alpinelinux.org/alpine/aports/-/commits/master">Read more</a>
        </div>
    </div>

</div> <!-- end pure-g -->


            </div> <!-- end content -->
            <footer>&copy; Copyright 2026 Alpine Linux Development Team all rights reserved | <a href="/privacy-policy.html">Privacy Policy</a></footer>
        </div> <!-- end wrapper -->
    </body>
</html>
* Connection #0 to host alpinelinux.org left intact
```

---

### A.2. Запит без захисту з'єднання

**Команда:**

```
curl -v http://neverssl.com
```

**Вивід:**

```
* Host neverssl.com:80 was resolved.
* IPv6: (none)
* IPv4: 34.223.124.45
*   Trying 34.223.124.45:80...
* Connected to neverssl.com (34.223.124.45) port 80
> GET / HTTP/1.1
> Host: neverssl.com
> User-Agent: curl/8.7.1
> Accept: */*
> 
* Request completely sent off
< HTTP/1.1 200 OK
< Date: Sun, 20 Sep 2026 19:14:01 GMT
< Server: Apache/2.4.68 ()
< Upgrade: h2,h2c
< Connection: Upgrade
< Last-Modified: Wed, 29 Jun 2022 00:23:33 GMT
< ETag: "f79-5e28b29d38e93"
< Accept-Ranges: bytes
< Content-Length: 3961
< Vary: Accept-Encoding
< Content-Type: text/html; charset=UTF-8
< 
<html>
	<head>
		<title>NeverSSL - Connecting ... </title>
		<style>
		body {
			font-family: Montserrat, helvetica, arial, sans-serif;
			font-size: 16x;
			color: #444444;
			margin: 0;
		}
		h2 {
			font-weight: 700;
			font-size: 1.6em;
			margin-top: 30px;
		}
		p {
			line-height: 1.6em;
		}
		.container {
			max-width: 650px;
			margin: 20px auto 20px auto;
			padding-left: 15px;
			padding-right: 15px
		}
		.header {
			background-color: #42C0FD;
			color: #FFFFFF;
			padding: 10px 0 10px 0;
			font-size: 2.2em;
		}
		.notice {
			background-color: red;
			color: white;
			padding: 10px 0 10px 0;
			font-size: 1.25em;
			animation: flash 4s infinite;
		}
		@keyframes flash {
		0% {
			background-color: red;
		}
		50% {
			background-color: #AA0000;
		}
		0% {
			background-color: red;
		}
		}
		<!-- CSS from Mark Webster https://gist.github.com/markcwebster/9bdf30655cdd5279bad13993ac87c85d -->
		</style>

		<script>
			var adjectives = [ 'cool' , 'calm' , 'relaxed', 'soothing', 'serene', 'slow',
							'beautiful', 'wonderful', 'wonderous', 'fun', 'good',
							'glowing', 'inner', 'grand', 'majestic', 'astounding',
							'fine', 'splendid', 'transcendent', 'sublime', 'whole',
							'unique', 'old', 'young', 'fresh', 'clear', 'shiny',
							'shining', 'lush', 'quiet', 'bright', 'silver' ];

			var nouns =	  [ 'day', 'dawn', 'peace', 'smile', 'love', 'zen', 'laugh',
							'yawn', 'poem', 'song', 'joke', 'verse', 'kiss', 'sunrise',
							'sunset', 'eclipse', 'moon', 'rainbow', 'rain', 'plan',
							'play', 'chart', 'birds', 'stars', 'pathway', 'secret',
							'treasure', 'melody', 'magic', 'spell', 'light', 'morning'];

			var prefix =
					// Choose 3 zen adjectives
					adjectives.sort(function(){return 0.5-Math.random()}).slice(-3).join('')
					+
					// Coupled with a zen noun
					nouns.sort(function(){return 0.5-Math.random()}).slice(-1).join('');
			window.location.href = 'http://' + prefix + '.neverssl.com/online';
		</script>
	</head>
	<body>
	<noscript>
		<div class="notice">
			<div class="container">
				⚠️ JavaScript appears to be disabled. NeverSSL's cache-busting works better if you enable JavaScript for <code>neverssl.com</code>.
			</div>
		</div>
	</noscript>
	<div class="header">
		<div class="container">
		<h1>NeverSSL</h1>
		</div>
	</div>
	<div class="content">
	<div class="container">

	<h1 id="status"></h1>
	<script>document.querySelector("#status").textContent = "Connecting ...";</script>
	<noscript>

		<h2>What?</h2>
		<p>This website is for when you try to open Facebook, Google, Amazon, etc
		on a wifi network, and nothing happens. Type "http://neverssl.com"
		into your browser's url bar, and you'll be able to log on.</p>

		<h2>How?</h2>
		<p>neverssl.com will never use SSL (also known as TLS). No
		encryption, no strong authentication, no <a
		href="https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security">HSTS</a>,
		no HTTP/2.0, just plain old unencrypted HTTP and forever stuck in the dark
		ages of internet security.</p>

		<h2>Why?</h2>
		<p>Normally, that's a bad idea. You should always use SSL and secure
		encryption when possible. In fact, it's such a bad idea that most websites
		are now using https by default.</p>

		<p>And that's great, but it also means that if you're relying on
		poorly-behaved wifi networks, it can be hard to get online.  Secure
		browsers and websites using https make it impossible for those wifi
		networks to send you to a login or payment page. Basically, those networks
		can't tap into your connection just like attackers can't. Modern browsers
		are so good that they can remember when a website supports encryption and
		even if you type in the website name, they'll use https.</p>

		<p>And if the network never redirects you to this page, well as you can
		see, you're not missing much.</p>

        <a href="https://twitter.com/neverssl">Follow @neverssl</a>

	</noscript>

	</div>
	</div>

	</body>
</html>
* Connection #0 to host neverssl.com left intact
```

---

### A.3. Запит до служби доменних імен

*Windows: `Resolve-DnsName ВАШ_ДОМЕН`*

**Команда (перше виконання):**

```
dig alpinelinux.org
```

**Вивід:**

```
; <<>> DiG 9.10.6 <<>> alpinelinux.org
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 727
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;alpinelinux.org.		IN	A

;; ANSWER SECTION:
alpinelinux.org.	1216	IN	A	213.219.36.190

;; Query time: 61 msec
;; SERVER: 193.41.60.1#53(193.41.60.1)
;; WHEN: Sun Sep 20 22:19:26 EEST 2026
;; MSG SIZE  rcvd: 60
```

**Команда (повторне виконання через 5–7 хвилин):**

```
dig alpinelinux.org
```

**Вивід:**

```
; <<>> DiG 9.10.6 <<>> alpinelinux.org
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 48461
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;alpinelinux.org.		IN	A

;; ANSWER SECTION:
alpinelinux.org.	872	IN	A	213.219.36.190

;; Query time: 23 msec
;; SERVER: 193.41.60.1#53(193.41.60.1)
;; WHEN: Sun Sep 20 22:25:10 EEST 2026
;; MSG SIZE  rcvd: 60
```

**Зафіксовані значення:**

| Параметр | Перше виконання | Повторне виконання |
|---|---|---|
| Час виконання (год:хв) |22:19 |22:25 |
| IP-адреса |213.219.36.190 |213.219.36.190 |
| Значення TTL |1216 |872 |

---

### A.4. Контрольний ресурс

**Команда:**

```
curl -v https://google.com
```

**Вивід:**

```
* Host google.com:443 was resolved.
* IPv6: (none)
* IPv4: 142.250.120.101, 142.250.120.100, 142.250.120.138, 142.250.120.113, 142.250.120.102, 142.250.120.139
*   Trying 142.250.120.101:443...
* Connected to google.com (142.250.120.101) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* (304) (IN), TLS handshake, Unknown (8):
* (304) (IN), TLS handshake, Certificate (11):
* (304) (IN), TLS handshake, CERT verify (15):
* (304) (IN), TLS handshake, Finished (20):
* (304) (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / AEAD-CHACHA20-POLY1305-SHA256 / [blank] / UNDEF
* ALPN: server accepted h2
* Server certificate:
*  subject: CN=*.google.com
*  start date: Sep  4 08:04:49 2026 GMT
*  expire date: Nov 27 08:04:48 2026 GMT
*  subjectAltName: host "google.com" matched cert's "google.com"
*  issuer: C=US; O=Google Trust Services; CN=WE2
*  SSL certificate verify ok.
* using HTTP/2
* [HTTP/2] [1] OPENED stream for https://google.com/
* [HTTP/2] [1] [:method: GET]
* [HTTP/2] [1] [:scheme: https]
* [HTTP/2] [1] [:authority: google.com]
* [HTTP/2] [1] [:path: /]
* [HTTP/2] [1] [user-agent: curl/8.7.1]
* [HTTP/2] [1] [accept: */*]
> GET / HTTP/2
> Host: google.com
> User-Agent: curl/8.7.1
> Accept: */*
> 
* Request completely sent off
< HTTP/2 301 
< location: https://www.google.com/
< content-type: text/html; charset=UTF-8
< content-security-policy-report-only: object-src 'none';base-uri 'self';script-src 'nonce-EhmUJ8J9ter3373o0RREng' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp
< date: Sun, 20 Sep 2026 19:35:32 GMT
< expires: Tue, 20 Oct 2026 19:35:32 GMT
< cache-control: public, max-age=2592000
< server: gws
< content-length: 220
< x-xss-protection: 0
< x-frame-options: SAMEORIGIN
< alt-svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000
< 
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="https://www.google.com/">here</A>.
</BODY></HTML>
* Connection #0 to host google.com left intact
```

---

### A.5. Ресурси з некоректною конфігурацією сертифіката

**Випадок 1**

```
curl -v https://expired.badssl.com
```

```
* Host expired.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* Connected to expired.badssl.com (104.154.89.105) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (OUT), TLS alert, certificate expired (557):
* SSL certificate problem: certificate has expired
* Closing connection
* TLSv1.2 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (OUT), TLS alert, certificate expired (557):
curl: (60) SSL certificate problem: certificate has expired
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the web page mentioned above.
```

**Випадок 2**

```
curl -v https://wrong.host.badssl.com
```

```
* Host wrong.host.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* Connected to wrong.host.badssl.com (104.154.89.105) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (IN), TLS handshake, Server key exchange (12):
* TLSv1.2 (IN), TLS handshake, Server finished (14):
* TLSv1.2 (OUT), TLS handshake, Client key exchange (16):
* TLSv1.2 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.2 (OUT), TLS handshake, Finished (20):
* TLSv1.2 (IN), TLS change cipher, Change cipher spec (1):
* TLSv1.2 (IN), TLS handshake, Finished (20):
* SSL connection using TLSv1.2 / ECDHE-RSA-AES128-GCM-SHA256 / [blank] / UNDEF
* ALPN: server accepted http/1.1
* Server certificate:
*  subject: CN=*.badssl.com
*  start date: Jul 28 20:03:02 2026 GMT
*  expire date: Oct 26 20:03:01 2026 GMT
*  subjectAltName does not match host name wrong.host.badssl.com
* SSL: no alternative certificate subject name matches target host name 'wrong.host.badssl.com'
* Closing connection
* TLSv1.2 (OUT), TLS alert, close notify (256):
curl: (60) SSL: no alternative certificate subject name matches target host name 'wrong.host.badssl.com'
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the web page mentioned above.
```

**Випадок 3**

```
curl -v https://self-signed.badssl.com
```

```
* Host self-signed.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* Connected to self-signed.badssl.com (104.154.89.105) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (OUT), TLS alert, unknown CA (560):
* SSL certificate problem: self signed certificate
* Closing connection
* TLSv1.2 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (OUT), TLS alert, unknown CA (560):
curl: (60) SSL certificate problem: self signed certificate
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the web page mentioned above.
```

---

## Частина B. Власна модель рівнів

**Кількість виділених груп:** ___

| № | Назва групи (власне формулювання) | Рядки виводу, віднесені до групи | Обґрунтування |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |
| 7 | | | |

*Групи впорядковано від найближчої до користувача (№ 1) до найближчої до апаратного забезпечення. Зайві рядки вилучити, за потреби — додати.*

**Рядки, які не вдалося віднести до жодної групи:**

| Рядок виводу | Причина утруднення |
|---|---|
| | |
| | |
| | |

---

## Контрольні питання

**1. Скільки рядків діагностичного виводу передує отриманню даних сторінки (завдання A.1)?**

> 

**2. Які рядки наявні у виводі A.1 і відсутні у виводі A.2? Чим це зумовлено?**

> 

**3. Звідки у виводі з'явилося значення `443`, якщо його не було вказано в адресі?**

> 

**4. Як змінилося значення TTL між двома запитами (A.3)? Що означає це число?**

> 

**5. Чим відрізняються між собою три причини помилок із завдання A.5? Сформулювати кожну однією фразою.**

| Випадок | Причина недовіри |
|---|---|
| `expired` | |
| `wrong.host` | |
| `self-signed` | |

**6. Три рядки з власних виводів, про які не йшлося на лекції 1:**

| № | Рядок виводу | Джерело (номер завдання) |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |

*Пояснення до цих рядків не потрібне.*

---

## Висновки

*150–300 слів. Спиратися на власні спостереження, а не на матеріал лекції.*

**D.1. Що виявилося неочевидним або несподіваним**

*Назвати конкретно, з посиланням на рядок виводу.*

> 

**D.2. Чому саме така кількість груп у частині B**

*На якій підставі ухвалено рішення. Що змусило б його змінити.*

> 

**D.3. Питання, яке залишилося без відповіді**

> 

---

## Використання штучного інтелекту

*Розділ обов'язковий. Заповнюється незалежно від того, чи використовувався ШІ. Детальні вимоги — у документі «Політика використання технологій штучного інтелекту».*

**Факт використання:** використано / не використано *(потрібне залишити)*

**Установлений рівень для цієї роботи:** Р3 — ШІ як співвиконавець

**Фактичний рівень використання:** Р___

### Використані системи

| Система | Версія або модель | Період використання |
|---|---|---|
| | | |

### Промпти

*Наводити дослівно, у тому вигляді, у якому запит було надано системі. Переказ не приймається.*

| № | Розділ роботи | Текст промпта |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |

### Дії з отриманим результатом

| № промпта | Що перевірено | Що змінено | Що відхилено і чому |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

### Підтвердження

Підтверджую, що всі наведені в цьому звіті виводи команд отримано мною особисто внаслідок фактичного виконання відповідних дій, а відомості цього розділу є повними та достовірними.

> Виводи `curl`, `dig` та інші артефакти не можуть бути згенеровані. Це стосується будь-якого рівня використання ШІ.

---

## Примітки виконавця

*(необов'язковий розділ: що не спрацювало, які команди довелося змінити, які виникли труднощі)*

>
