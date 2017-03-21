# Slides

This repository holds a number of slides created with the free open source tool [reveal.js](https://github.com/hakimel/reveal.js)

you can watch that slides here: [https://services.ub.uni-leipzig.de/slides/](https://services.ub.uni-leipzig.de/slides/)

## create a new slide

* clone the source code
```bash
$# git clone git@github.com:ubleipzig/reveal.js.git
```
* copy one of the html files in the root folder and name it according to your presentation
* if you use images, copy them to `images/your-presentation-name/*`
* create your slides using [reveal.js](https://github.com/hakimel/reveal.js)` vast possibilities
* add your slide to as a new section to the `index.html`
```html
<section>
  <img data-src="images/awesome-presentation/awesome-logo.png" height="200px">
  <h2>
    <a href="awesome-presentation.html" target="_blank">The Awesome Presentation</a>
  </h2>
  <dl>
    <dt>
      a brief description about this presentation and why it is awesome.
    </dt>
    <dd>
      <small>
        <table>
          <tr>
            <th>Autor:</th><td>Your Name &lt;your-email@ub.uni-leipzig.de&gt;</td>
          </tr>
          <tr>
            <th>erstellt am:</th><td>21.05.2017</td>
          </tr>
        </table>
      </small>
    </dd>
  </dl>
</section>
```
* commit and push the project
* after our automatic deploy process you can find your presentation at the link already mentioned above

## local authoring
In order to view your slides while creating them you can simply open the html-page in your browser.
However, some features i.e. side notes and pdf-creation only work when requested via http. For this
purpose you can use docker to start a container that is serving the slides as a webserver.

* first install depending node modules
```bash
$# docker-compose run --rm node npm install
```
* then start the service
```bash
$# docker-compose up
```

It also compiles your css if you choose to create a custom theme. If you just want to compile the css
prior to committing your changes use

```bash
$# docker-compose run --rm node npm run compile-css
```

## local copy
If you want to use the slides offline you can just open the html-page which is the entrypoint for your slides
locally in your browser.