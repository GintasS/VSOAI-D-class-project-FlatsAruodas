<div align="center">
  <h2>Vilnius School of AI - D class final project - Aruodas.lt flats listings</h2>
</div>

## Jump to...

  - [Intro](#intro)
  - [Features](#features)
  - [Units](#units)
  - [Media](#media)
  - [Changelog](#changelog)

## <a name="Intro"></a>Intro

<p>This is a final project for D class graduation, where I scraped <a href='https://www.aruodas.lt/' target='_blank'>aruodas.lt</a>, a lithuanian real estate website, for all available flat listings(ads).<br>Url for all flats: <a href='https://www.aruodas.lt/butai/' target='_blank'>https://www.aruodas.lt/butai/</a>.<br><br>
Scrap was conducted on <b>2019-08-24</b>.
</p>

## <a name="Features"></a>Features

<ul>
  <li>9687 rows</li>
  <li>27 columns(22 after cleaning)</li>
  <li><a href='https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm' target='_blank'>k-nearest neighbors</a> algorithm to predict <b>Building Type</b></li>
  <li>All main units in one place</li>
  <li>Currency support</li>
  <li>SMS support(trial)</li>
  <li>Works offline</li>
  <li>Some Unit Tests!</li>
</ul>

## <a name="AboutSms"></a>About SMS

<p>I implemented a feature where one can message an SMS endpoint and receive unit conversion via SMS message!<br>I use Twilio provider's trial version and thus it has limitations, like you can't send SMS messages to not trusted numbers.<br>You can see it in action from the demos below.<br><br><b>Structure:</b><code>unit category/unit from/unit to/amount</code><br><b>Example:</b> mass/kilogram/gram/1</p>

## <a name="Units"></a>Units
<ul>
  <li>Time</li>
  <li>Electric current</li>
  <li>Mass</li>
  <li>Length</li>
  <li>Temperature</li>
  <li>Luminous intensity</li>
  <li>Currencies(USD, EUR and more)</li>
</ul>

## <a name="Media"></a>Media

<a target="_blank" href="https://github.com/GintasS/VSOAI-project/blob/master/media/Base.JPG">
  <img src="https://github.com/GintasS/VSOAI-project/blob/master/media/Base.JPG" height="300" style="max-width:50%;"></img>
</a>
<blockquote>Base window.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-project/blob/master/media/Image2.JPG">
  <img src="https://github.com/GintasS/VSOAI-project/blob/master/media/Image2.JPG" height="200" style="max-width:30%;"></img>
</a>
<blockquote>Conversion from fortnight to hours.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-project/blob/master/media/Image3.JPG">
  <img src="https://github.com/GintasS/VSOAI-project/blob/master/media/Image3.JPG" height="200" style="max-width:60%;"></img>
</a>
<blockquote>Conversion from EUR to RUB.</blockquote>
<blockquote>Conversion from fortnight to hours.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-project/blob/master/media/Image4.JPG">
  <img src="https://github.com/GintasS/VSOAI-project/blob/master/media/Image4.JPG" height="200" style="max-width:60%;"></img>
</a>
<blockquote>Conversion from mace to gram.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-project/blob/master/media/demo3.gif">
  <img src="https://github.com/GintasS/VSOAI-project/blob/master/media/demo3.gif" height="400" style="max-width:60%;"></img>
</a>
<blockquote>Conversion via SMS: 1 kilogram to grams.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-project/blob/master/media/demo4.gif">
  <img src="https://github.com/GintasS/VSOAI-project/blob/master/media/demo4.gif" height="400" style="max-width:60%;"></img>
</a>
<blockquote>Conversion via SMS: 1 kilometre to metre.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-project/blob/master/media/demo5.gif">
  <img src="https://github.com/GintasS/VSOAI-project/blob/master/media/demo5.gif" height="400" style="max-width:60%;"></img>
</a>
<blockquote>Conversion via SMS: edge cases.</blockquote>

## <a name="Changelog"></a>Changelog

<h3>CHANGELOG 7/7/2019</h3>
<ul>
  <li>Moved project from console application to Flask.</li>
  <li>Added basic interface for selecting categories, units, amounts.</li>  
</ul>

<h3>CHANGELOG 18/7/2019</h3>
<ul>
  <li>Added more unit types.</li>
  <li>Fixed main layout of the MVP.</li>
  <li>Code improvements.</li>
</ul>
