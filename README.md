<h1 align="center">
  <br>
  <a href="https://github.com/s0md3v/XSStrike"><img src="https://image.ibb.co/cpuYoA/xsstrike-logo.png" alt="XSStrike"></a>
  <br>
  XSStrike
  <br>
</h1>

<h4 align="center">Advanced XSS Detection Suite</h4>

<p align="center">
  <a href="https://github.com/s0md3v/XSStrike/releases">
    <img src="https://img.shields.io/github/release/s0md3v/XSStrike.svg">
  </a>
  <a href="https://travis-ci.com/s0md3v/XSStrike">
    <img src="https://img.shields.io/travis/com/s0md3v/XSStrike.svg">
  </a>
  <a href="https://github.com/s0md3v/XSStrike/issues?q=is%3Aissue+is%3Aclosed">
      <img src="https://img.shields.io/github/issues-closed-raw/s0md3v/XSStrike.svg">
  </a>
</p>

![multi xss](https://image.ibb.co/gOCV5L/Screenshot-2018-11-19-13-33-49.png)

<p align="center">
  <a href="https://github.com/s0md3v/XSStrike/wiki">XSStrike Wiki</a> •
  <a href="https://github.com/s0md3v/XSStrike/wiki/Usage">Usage</a> •
  <a href="https://github.com/s0md3v/XSStrike/wiki/FAQ">FAQ</a> •
  <a href="https://github.com/s0md3v/XSStrike/wiki/For-Developers">For Developers</a> •
  <a href="https://github.com/s0md3v/XSStrike/wiki/Compatibility-&-Dependencies">Compatibility</a> •
  <a href="https://github.com/s0md3v/XSStrike#gallery">Gallery</a>
</p>

XSStrike is a Cross Site Scripting detection suite equipped with four hand written parsers, an intelligent payload generator, a powerful fuzzing engine and an incredibly fast crawler.

Instead of injecting payloads and checking it works like all the other tools do, XSStrike analyses the response with multiple parsers and then crafts payloads that are guaranteed to work by context analysis integrated with a fuzzing engine.
Here are some examples of the payloads generated by XSStrike:
```
}]};(confirm)()//\
<A%0aONMouseOvER%0d=%0d[8].find(confirm)>z
</tiTlE/><a%0donpOintErentER%0d=%0d(prompt)``>z
</SCRiPT/><DETAILs/+/onpoINTERenTEr%0a=%0aa=prompt,a()//
```
Apart from that, XSStrike has crawling, fuzzing, parameter discovery, WAF detection capabilities as well. It also scans for DOM XSS vulnerabilities.

### Main Features
- Reflected and DOM XSS scanning
- Multi-threaded crawling
- Context analysis
- Configurable core
- WAF detection & evasion
- Outdated JS lib scanning
- Intelligent payload generator
- Handmade HTML & JavaScript parser
- Powerful fuzzing engine
- Blind XSS support
- Highly researched work-flow
- Complete HTTP support
- Bruteforce payloads from a file
- Powered by [Photon](https://github.com/s0md3v/Photon), [Zetanize](https://github.com/s0md3v/zetanize) and [Arjun](https://github.com/s0md3v/Arjun)
- Payload Encoding

### Documentation
- [Usage](https://github.com/s0md3v/XSStrike/wiki/Usage)
- [Compatibility & Dependencies](https://github.com/s0md3v/XSStrike/wiki/Compatibility-&-Dependencies)

### FAQ
- [It says fuzzywuzzy isn't installed but it is.](https://github.com/s0md3v/XSStrike/wiki/FAQ#it-says-fuzzywuzzy-is-not-installed-but-its)
- [What's up with Blind XSS?](https://github.com/s0md3v/XSStrike/wiki/FAQ#whats-up-with-blind-xss)
- [Why XSStrike boasts that it is the most advanced XSS detection suite?](https://github.com/s0md3v/XSStrike/wiki/FAQ#why-xsstrike-boasts-that-it-is-the-most-advanced-xss-detection-suite)
- [I like the project, what enhancements and features I can expect in future?](https://github.com/s0md3v/XSStrike/wiki/FAQ#i-like-the-project-what-enhancements-and-features-i-can-expect-in-future)
- [What's the false positive/negative rate?](https://github.com/s0md3v/XSStrike/wiki/FAQ#whats-the-false-positivenegative-rate)
- [Tool xyz works against the target, while XSStrike doesn't!](https://github.com/s0md3v/XSStrike/wiki/FAQ#tool-xyz-works-against-the-target-while-xsstrike-doesnt)
- [Can I copy it's code?](https://github.com/s0md3v/XSStrike/wiki/FAQ#can-i-copy-its-code)
- [What if I want to embed it into a proprietary software?](https://github.com/s0md3v/XSStrike/wiki/FAQ#what-if-i-want-to-embed-it-into-a-proprietary-software)

### Docker Build

 ```
 $ docker build -t <IMAGE NAME> .
 OR
 $ docker build -t xshuden/xsstrike .
 ```

### Docker Usage

 ```
 $ docker run --rm -it xshuden/xsstrike
 $ docker run --rm -it xshuden/xsstrike -u https://xss-game.appspot.com/level1/frame?query=
 ```

### Gallery
#### DOM XSS
![dom xss](https://image.ibb.co/bQaQ5L/Screenshot-2018-11-19-13-48-19.png)
#### Reflected XSS
![multi xss](https://image.ibb.co/gJogUf/Screenshot-2018-11-19-14-19-36.png)
#### Crawling
![crawling](https://image.ibb.co/e6Rezf/Screenshot-2018-11-19-13-50-59.png)
#### Fuzzing
![fuzzing](https://image.ibb.co/fnhuFL/Screenshot-2018-11-19-14-04-46.png)
#### Bruteforcing payloads from a file
![bruteforcing](https://image.ibb.co/dy5EFL/Screenshot-2018-11-19-14-08-36.png)
#### Interactive HTTP Headers Prompt
![headers](https://image.ibb.co/ecNph0/Screenshot-2018-11-19-14-29-35.png)
#### Hidden Parameter Discovery
![arjun](https://image.ibb.co/effjh0/Screenshot-2018-11-19-14-16-51.png)

### Contribution, Credits & License
Ways to contribute
- Suggest a feature
- Report a bug
- Fix something and open a pull request
- Create a browser extension
- Create a burp suite/zaproxy plugin
- Help me document the code
- Spread the word

Licensed under the GNU GPLv3, see [LICENSE](LICENSE) for more information.

The WAF signatures in `/db/wafSignatures.json` are taken & modified from [sqlmap](https://github.com/sqlmapproject/sqlmap). I extracted them from sqlmap's waf detection modules which can found [here](https://github.com/sqlmapproject/sqlmap/blob/master/waf/) and converted them to JSON.\
`/plugins/retireJS.py` is a modified version of [retirejslib](https://github.com/FallibleInc/retirejslib/).
