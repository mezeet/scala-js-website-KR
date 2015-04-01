---
layout: page
title: Scala.js
tagline: the Scala to JavaScript compiler
---
{% include JB/setup %}

<img id="front-page-logo" alt="Scala.js logo" title="Scala.js logo"
    src="{{ BASE_PATH }}/images/scala-js-logo.svg" />

스칼라.js 는 스칼라 코드를 자바스크립트로 컴파일 해서, 당신이 웹 어플리케이션을 전체적으로 스칼라로 작성하게 해줍니다. [프로젝트 갤러리](#built_with_scalajs) 에서 Scala.js 로 어떤 종류의 일을 할 수 있는 지 둘러 보세요.

##시작하기

<span><a href="{{ BASE_PATH }}/doc/tutorial.html" class="btn btn-large btn-success">지침서 시작</a></span>
&nbsp;&nbsp;&nbsp;
<span><a href="http://www.scala-js-fiddle.com/" class="btn btn-large btn-success">브라우저에서 시도해봐</a></span>

시작하는 가장 쉬운 방법은 우리의 [지침서](./doc/tutorial.html)를 따르는 것입니다. 당신은 또한
[부트스트래핑 뼈대](https://github.com/sjrd/scala-js-example-app)를 포크하고 readme 내부에 지침을 따르거나 [브라우저에서 시도](http://www.scala-js-fiddle.com/)할 수 있습니다. 또한 당신이 시작하는데 도움이 될 만한 입문 자료를 많이 포함하고 있는  [Scala.js 시도하기](https://lihaoyi.github.io/hands-on-scala-js) 이북도 있습니다.

우리는 또한 SBT 를 요구하지 않는 [독립 디스트리뷰션](./downloads.html) 도 있습니다.

_Note Scala.js 는 Typesafe Reactive 플랫폼의 일부가 아닙니다. 더해서, 우리는 Scala.js 가 실서비스-가능하다고 판단하지만, Typesafe 그것을 지원하기 위해 어떤 상업적인 것도 지원하지 않을 것입니다._

*역자 주* : Typesafe 사는 스칼라 언어 창시자가 공동 창업자인 회사입니다.


## 주목할만한 기능

*   스칼라의 모든 것 지원(매크로 포함!),
    modulo [몇 몇 분법적 차이](./doc/semantics.html)
*   매우 좋은 [자바스크립트 와의 상호운용성](./doc/js-interoperability.html).
    예를 들자면 jQuery 와 HTML5 를 당신의 스칼라.js 코드에서 사용하며, 타입지정 혹은 미지정 방법 
    모두 사용할 수 있습니다. 혹은 스칼라.js 객체를 생성하고 그 메서드를 자바스크립트에서
    호출 가능합니다.
*   [sbt에 통합됨](./doc/sbt-plugin.html)
    (의존성 관리와 증분 컴파일 지원을 포함합니다.)
*   당신이 좋아하는 스칼라용 IDE에서 사용 가능합니다.
*   [Source Maps] 을 생성해서(http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/)
    매끄러운 디버깅 경험을 제공합니다. (소스 맵을 제공하는 브라우저 내에서 당신의 스칼라
    코드를 단계별로 보세요.)
*   [Google Closure Compiler](https://developers.google.com/closure/compiler/)와 통합되어 프로덕션 환경을 위한 최소한의 코드를 생산합니다. 컴파일된 blobs 의 범위는 170-400kb 입니다.
*   (매우) 효율적인 자바스크립트 코드를 생산합니다.([benchmarks](https://github.com/sjrd/scalajs-benchmarks))

## 자원

*   [문서](./doc/): APIs, 지침서,레퍼런스.
*   [Stackoverflow 에 Scala.js 태그](http://stackoverflow.com/questions/tagged/scala.js): Scala.js를 사용하는 과정에서 생긴 기술적 질문들을 분리하기 위해.
*   [공식 메일링 리스트](https://groups.google.com/forum/?fromgroups#!forum/scala-js): 일반적인 토론, 아이디어, 라이브러리 소개 등
*   [Gitter 대화 방](https://gitter.im/scala-js/scala-js): Scala.js 사용자의 커뮤니티를 만나자 

Featured presentations to get you convinced:

*   [Hands-on Scala.js](http://vimeo.com/111978847) at Pacific North-West Scala 2014, by Li Haoyi
*   [Cross-Platform Development in Scala.js](https://www.youtube.com/watch?v=Ksoi6AG9nbA) at Scala by the Bay 2014, by Li Haoyi

## 라이브러리

이것은 Scala.js 와 함께 작동하는 것으로 알려진 라이브러리의 모음입니다.
`scala-js-dom` 과 `scala-js-jquery` 같은 것들은 자바스크립트에 특정적이고 JVM 에는 말이 되지 않습니다.

`scala-async` 같은 것들은 순수-매크로 프로젝트이고  이리하여 스칼라.js 와 함께 작동하면 발군입니다. 그것들 대부분은 JVM 과 JS 사이를 넘어 크로스 컴파일링 되고, 그리하여 각각 플랫폼에서 실행하기 위한 분리된 인공물을 가집니다.

### 자바스크립트 라이브러리를 위한 정적 타입들

*   [scalajs-dom](https://github.com/scala-js/scala-js-dom): DOM API를 위한 정적 타입, 몇 가지 확장을 더 가졌다.
*   [scalajs-jquery](https://github.com/scala-js/scala-js-jquery): jQuery 를 위한 정적 타입
*   [scalajs-pouchdb](https://github.com/chandu0101/scalajs-facades/tree/master/core/src/main/scala/chandu0101/scalajs/facades/pouchdb): PouchDB를 위한 정적 타입

### 테스팅 프레임워크

All these testing frameworks cross-compile on the JVM and JS.

*   [uTest](https://github.com/lihaoyi/utest)
*   [MiniTest](https://github.com/monifu/minitest)
*   [Little Spec](https://github.com/eecolor/little-spec)
*   [Nyaya](https://github.com/japgolly/nyaya): Property testing and related.
*   [zcheck](https://github.com/InTheNow/zcheck): A wrapper around scalacheck and scalaz's Speclite.
*   [Greenlight](https://github.com/greencatsoft/greenlight)

### HTML 템플레이딩 라이브러리

*   [Scalatags](https://github.com/lihaoyi/scalatags): cross-compiling HTML templating library/DSL that works on both Scala/JVM and Scala.js

### UI 프레임워크

*   [scalajs-react](https://github.com/japgolly/scalajs-react): Type-safe and Scala-friendly library over Facebook's [React](http://facebook.github.io/react/).
*   [scala-js-binding](https://github.com/antonkulaga/scala-js-binding): An all-Scala.js HTML binding library
*   [scalajs-angular](https://github.com/greencatsoft/scalajs-angular) with [TodoMvc example](https://github.com/greencatsoft/scalajs-angular-todomvc): static types and complementary API for AngularJS
*   [scalajs-angulate](https://github.com/jokade/scalajs-angulate): another binding to AngularJS with enhancements
*   [Widok](https://widok.github.io/): Reactive web framework for the JVM and Scala.js

### 직렬화/피클링 라이브러리

*   [uPickle](https://github.com/lihaoyi/upickle): cross-compiling statically-typed pickling (via typeclasses/macros) for both Scala/JVM and Scala.js
*   [Prickle](https://github.com/benhutchison/prickle): cross-compiling statically-typed pickling library with support for pickling object graphs containing shared objects and cycles
*   [Scala.js Pickling](https://github.com/scala-js/scala-js-pickling): cross-compiling pickling library based on explicit registration of picklers

### 클라이언트-서버 커뮤니케이션

*   [autowire](https://github.com/lihaoyi/autowire): 정적인-typed Ajax 호출과 RPCs 크로스 컴파하기

### 시각화

*   [Paths.scala.js](https://github.com/andreaferretti/paths-scala-js):SVG 차트와 모양을 생성하는 라이브러리(wrapper over [Paths.js](https://github.com/andreaferretti/paths-js))

### FRP/reactive 확장

*   [Scala.Rx](https://github.com/lihaoyi/scala.rx): cross-compiling change-propagation/FRP library
*   [Monifu](https://github.com/alexandru/monifu): cross-compiling reactive extensions (Rx) with back-pressure, atomic references and other multi-threading primitives

### 잘 알려진 스칼라 라이브러리 포츠(ports)

*   [NICTA/rng](https://github.com/japgolly/rng): 순수-함수 난수 생성
*   [Monocle](https://github.com/japgolly/Monocle): Haskell 에 강하게 영향을 받은 Optics 라이브러리 [Lens](https://github.com/ekmett/lens).
*   [Scalaz](https://github.com/japgolly/scalaz): 함수형 프로그래밍을 위한 라이브러리
*   [Shapeless](https://github.com/japgolly/shapeless): 스칼라를 위한 Generic 프로그래밍

###기타

*   [Scala-Async](https://github.com/scala/async) (works out-of-box with Scala.js)
*   Scalaxy [Loops](https://github.com/ochafik/Scalaxy/tree/master/Loops) and [Streams](https://github.com/ochafik/Scalaxy/tree/master/Streams) (work out-of-box with Scala.js)

## 뼈대

*   [workbench-예제-앱](https://github.com/lihaoyi/workbench-example-app): skeleton application using [Scala.js workbench](https://github.com/lihaoyi/scala-js-workbench) for live-reloading in the browser, together with a collection of sample applications developed using it
*   [Scala.js 로 Play! 어플리케이션](https://github.com/vmunier/play-with-scalajs-example)
*   [Scala.js 로 Node.js](https://github.com/rockymadden/scala-node-example)
*   [Scala.js 과 React SPA 튜토리얼](https://github.com/ochrons/scalajs-spa-tutorial):  scalajs-react, Spray 그리고 Bootstrap 위에서 구축된 간단한 단일 페이지 어플리케이션 지침서. 

## 도구

*   [Scala.js workbench](https://github.com/lihaoyi/scala-js-workbench): 브라우저에서 실시간 새로고침 해주는 Scala.js 프로젝트 용 sbt 플러그인 ([예제 앱](https://github.com/lihaoyi/workbench-example-app))

## 기타 

* [Port of the Dart benchmark harness](https://github.com/sjrd/scalajs-benchmarks)

## 공헌

* [Scala.js on GitHub](https://github.com/scala-js/scala-js)

## <a name="built_with_scalajs"></a> Scala.js 로 만들어짐

 Scala.js 를 사용해 만들어진 웹사이트:

* March 2015
  - [Doctus](http://entelijan.net/art/doctus/), a library for the creation of visual art pieces, by [Wolfgang Wagner](http://entelijan.net/)
* September 2014
  - [Weather Information System](https://github.com/knoldus/ScalaJs_Weather_Report), by [Ayush Mishra](https://www.linkedin.com/pub/ayush-mishra/23/87b/a27), [Knoldus Software LLP](http://www.knoldus.com/home.knol)
* July 2014
  - [Play and Scala.js Showcase](https://github.com/hussachai/play-scalajs-showcase), by Hussachai Puripunpinyo
* May 2014
  - [Papa-Carlo Incremental Parser Demo](http://lakhin.com/projects/papa-carlo/demo/), by Eliah-Lakhin
* April 2014
  - [Ray-Tracer](http://lihaoyi.github.io/workbench-example-app/raytracer.html), a ray-tracer written in Scala.js by Li Haoyi
* February 2014
  - [TodoMVC](http://lihaoyi.github.io/workbench-example-app/todo.html), an implementation of the [TodoMVC example application](http://todomvc.com/) using Scala.js, Scalatags, Scala.Rx and scala-js-dom, by Li Haoyi
  - [Sierpinski Triangle](http://lihaoyi.github.io/workbench-example-app/triangle.html) and [Dodge the dot](http://lihaoyi.github.io/workbench-example-app/dodge.html) (Scala.js workbench [example apps](https://github.com/lihaoyi/workbench-example-app)), by Li Haoyi
  - [Scala.jsFiddle](http://www.scala-js-fiddle.com/), an online scratchpad that lets you compile and run Scala.js snippets right in the browser, by Li Haoyi
* December 2013
  - [Roll](http://lihaoyi.github.io/roll/), a 2D Physics Platformer
    by Li Haoyi
* December 2013
  - [Sliding Puzzle](https://github.com/sebnozzi/sliding-puzzle)
    by [Sebastian Nozzi](http://www.sebnozzi.com/)
* October 2013
  - [Several games](http://lihaoyi.github.io/scala-js-games/)
    by Li Haoyi
* July 2013
  - [Knapsack on a graph](http://krishnanraman.github.io/scala-js/examples/helloworld/helloworld.html)
    by Krishnan Raman
* June 2013
  - [Collidium Online](http://collidium.shadaj.me/) by
    [@ShadajL](https://twitter.com/ShadajL)
* April 2013
  - The [Reversi]({{ BASE_PATH }}/examples/reversi/) example by Sébastien Doeraene


## 버전 내역

- [0.6.2](/news/2015/03/16/announcing-scalajs-0.6.2/)
- [0.6.1](/news/2015/03/03/announcing-scalajs-0.6.1/)
- [0.6.0](/news/2015/02/05/announcing-scalajs-0.6.0/)
- [0.6.0-RC2](/news/2015/01/23/announcing-scalajs-0.6.0-RC2/)
- [0.6.0-RC1](/news/2015/01/12/announcing-scalajs-0.6.0-RC1/)
- [0.6.0-M3](/news/2014/12/22/announcing-scalajs-0.6.0-M3/)
- [0.6.0-M2](/news/2014/12/05/announcing-scalajs-0.6.0-M2/)
- [0.6.0-M1](/news/2014/12/01/announcing-scalajs-0.6.0-M1/)
- [0.5.6](/news/2014/11/19/announcing-scalajs-0.5.6/)
- [0.5.5](/news/2014/09/18/announcing-scalajs-0.5.5/)
- [0.5.4](/news/2014/08/29/announcing-scalajs-0.5.4/)
- [0.5.3](/news/2014/07/30/announcing-scalajs-0.5.3/)
- [0.5.2](/news/2014/07/09/announcing-scalajs-0.5.2/)
- [0.5.1](/news/2014/06/30/announcing-scalajs-0.5.1/)
- [0.5.0](/news/2014/06/13/announcing-scalajs-0.5.0/)
- [0.4.4](https://groups.google.com/forum/#!searchin/scala-js/0.4.3/scala-js/ZVWU0NLxSI0/HUydhe56bA4J)
- [0.4.3](https://groups.google.com/forum/#!topic/scala-js/xnswQ7qHvjs)
- [0.4.2](https://groups.google.com/forum/#!topic/scala-js/apbxL1KHiTo)
- [0.4.1](https://groups.google.com/forum/#!topic/scala-js/urFh-U2K53U)
- [0.4.0](https://groups.google.com/forum/#!topic/scala-js/j9Ir4-_a1ls)
- [0.3](https://groups.google.com/forum/#!searchin/scala-js/0.3/scala-js/siSw-EsVy1w/6CzCE4WkCL0J)
- [0.2](https://groups.google.com/forum/#!searchin/scala-js/0.2/scala-js/ouSSRrBmrZE/Xx-pgAFrk7AJ)
- [0.1](http://www.scala-lang.org/news/2013/11/29/announcing-scala-js-v0.1.html)

##명예의 전당

* [Bug in node.js/v8](http://github.com/joyent/node/issues/7528) discovered by Scala.js through Scala test suite

<a href="https://github.com/scala-js/scala-js-website"><img style="position: absolute; top: 0; right: 0; border: 0;" src="https://s3.amazonaws.com/github/ribbons/forkme_right_orange_ff7600.png" alt="Fork me on GitHub"></a>
