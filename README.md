<div align="center">
  <h2>Vilnius School of AI - D class final project - Aruodas.lt flats listings</h2>
</div>

## Jump to...

  - [Intro](#intro)
  - [Features](#features)
  - [Libraries](#libraries)
  - [Column descriptions](#Columndescriptions)
  - [Media](#media)
  - [Machine Learning](#MachineLearning)
  - [Changelog](#Changelog)
  
## <a name="Intro"></a>Intro

<p>This is a final project for VSOAI D class graduation, where I web-scraped <a href='https://www.aruodas.lt/' target='_blank'>aruodas.lt</a>, a Lithuanian real-estate website, for all available flat listings(ads).</p>
<p>Url for all flats: <a href='https://www.aruodas.lt/butai/' target='_blank'>link</a>.</p>
<p>Scrap was conducted on <b>2019-08-24</b>.</p>

## <a name="Features"></a>Features

<ul>
  <li>9687 rows.</li>
  <li>27 columns(22 after cleaning).</li>
  <li>Data cleaning.</li>
  <li>Charts.</li>
  <li>Machine learning model: <br>
      <a href='https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm' target='_blank'>K-nearest neighbors</a> algorithm to predict <b>Building Type</b>.</li>
</ul>

## <a name="Libraries"></a>Libraries
<ul>
  <li>numpy</li>
  <li>pandas</li>
  <li>matplotlib</li>
  <li>seaborn</li>
  <li>folium</li>
  <li>scikit-learn</li>
</ul>

## <a name="Columndescriptions"></a>Column descriptions

<table>
  <tr>
    <th>Column name</th>
    <th>Description</th>
    <th>Example data</th>
  </tr>
  <tr><td>City</td><td>Flat's city/district/region</td><td>Vilnius</td></tr>
  <tr><td>County</td><td>Flat's district</td><td>Žirmūnai</td></tr>
  <tr><td>Street</td><td>Street name</td><td>Antakalnio g.</td></tr>
  <tr><td>HouseCount</td><td>A paid service, where you can <br>move up your real-estate listing via buying special "houses" on the ad.<br>
    This number indicates how many of those houses were bought.</td><td>1</td></tr>
  <tr><td>Link</td><td>Flat's unique link for the actual listing.</td><td>https://www.aruodas.lt/</td></tr>
  <tr><td>Price EUR</td><td>Flat's price in EUR</td><td>50000</td></tr>  
  <tr><td>Price per m2</td><td>Flat's price per square metre(m2)</td><td>5000</td></tr>
  <tr><td>Rooms</td><td>Flat's total room count</td><td>3</td></tr>  
  <tr><td>Area m2</td><td>Flat's area in square metres(m2)</td><td>45.10</td></tr>
  <tr><td>Floor</td><td>Flat's floor number in the building</td><td>3</td></tr>  
  <tr><td>Total floors</td><td>Total floors in the flat's building</td><td>5</td></tr>
  <tr><td>Flat number</td><td>(Removed in the notebook) Flat's house number</td><td>5</td></tr>  
  <tr><td>House number</td><td>(Removed in the notebook) Flat's number in the building</td><td>5A</td></tr>
  <tr><td>Year</td><td>Flat's building construction date. Date format: YYYY</td><td>1988</td></tr>
  <tr><td>Building type</td><td>Building type</td><td>Mūrinis</td></tr>
  <tr><td>Heating</td><td>Heating type</td><td>Centrinis kolektorinis</td></tr>
  <tr><td>Installation type</td><td>Finishing type</td><td>Dalinė apdaila</td></tr>
  <tr><td>Specials</td><td>Special items that describe a flat, e.g. <br>
      flat can have new plumbing installed</td><td>Nauja kanalizacija</td></tr>  
  <tr><td>Extra quarters</td><td>Special rooms that a flat has, e.g. a balcony</td><td>Balkonas</td></tr>
  <tr><td>Extra equipment</td><td>Extra equipment that comes with a flat, e.g. dishwasher</td><td>Plastikiniai vamzdžiai</td></tr>  
  <tr><td>Security</td><td>Describes the security measures that a particular flat employs, e.g. alarm</td><td>Šarvuotos durys</td></tr>
  <tr><td>Upload date</td><td>Ad upload date. Date format: YYYY-MM-DD</td><td>2019-08-21</td></tr>  
  <tr><td>Modify date</td><td>Ad modification date. Date format: YYYY-MM-DD</td><td>2019-08-21</td></tr>
  <tr><td>Memorized count</td><td>How many people saved(bookmarked) the ad</td><td>1</td></tr>   
  <tr><td>Views</td><td>Ad view count</td><td>345</td></tr>
  <tr><td>Telephone</td><td>Flat owner's/realtor's phone number</td><td>37000000000</td></tr>
  <tr><td>Coordinates</td><td>Flat's latitude and longitude coordinates in this order</td><td>54.000000 25.000000</td></tr>
 </table>
 
## <a name="MachineLearning"></a>Machine Learning
<p>I added a machine learning model - <a href='https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm' target='_blank'>K-nearest neighbors</a> algorithm to predict <b>Building Type</b> based on these factors(columns):<br>
  <ul>
     <li>Rooms</li>
     <li>Area</li>
     <li>Floor</li>
     <li>Total floors</li> 
     <li>Year</li>
  </ul>
Example & tutorial can be found here: <a href='https://stackabuse.com/k-nearest-neighbors-algorithm-in-python-and-scikit-learn/' target='_blank'>URL</a><br><br>
<b>Input dataframe (first 5 rows):</b><br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/tables/ML%20model%20dataframe.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/tables/ML%20model%20dataframe.JPG" height="170" style="max-width:50%;"></img>
</a><br><br>
<b>Model results:</b><br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/tables/ML%20model%20results.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/tables/ML%20model%20results.JPG" height="220" style="max-width:50%;"></img>
</a><br><br>
<b>Error rate k value chart:</b><br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/error%20rate%20k-value.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/error%20rate%20k-value.JPG" height="300" style="max-width:50%;"></img>
</a>
</p>

## <a name="Media"></a>Media

<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/flat%20prices%20histogram.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/flat%20prices%20histogram.JPG" height="300" style="max-width:50%;"></img>
</a>
<blockquote>Flat price histograms.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/flat%20uploads%20by%20date%20of%20week.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/flat%20uploads%20by%20date%20of%20week.JPG" height="300" style="max-width:50%;"></img>
</a>
<blockquote>Flats by the day of week.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/error%20rate%20k-value.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/error%20rate%20k-value.JPG" height="300" style="max-width:50%;"></img>
</a>
<blockquote>Error rate k value(for Machine Learning model).</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/flats%20by%20building%20type.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/flats%20by%20building%20type.JPG" height="300" style="max-width:50%;"></img>
</a>
<blockquote>Flats by building type.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/old%20town%20districts%20in%20top-3%20biggest%20cities%20and%20their%20average%20flat%20prices.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/old%20town%20districts%20in%20top-3%20biggest%20cities%20and%20their%20average%20flat%20prices.JPG" height="300" style="max-width:50%;"></img>
</a>
<blockquote>Average flat prices in the Top-3 Old town districts.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/top-10%20cities%20and%20districts%20by%20flats.JPG">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/charts/top-10%20cities%20and%20districts%20by%20flats.JPG" height="300" style="max-width:50%;"></img>
</a>
<blockquote>Top-10 cities and districts by flat count.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/maps/flats%20map.gif">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/maps/flats%20map.gif" height="400" style="max-width:50%;"></img>
</a>
<blockquote>Interactive map.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/maps/live%20map%20of%20flats%20listings%202019-08-18%20--%202019-08-24.gif">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/maps/live%20map%20of%20flats%20listings%202019-08-18%20--%202019-08-24.gif" height="400" style="max-width:50%;"></img>
</a>
<blockquote>Interactive map of flat listings in the 2019-08-18 - 2019-08-24 period.</blockquote>
<br>
<a target="_blank" href="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/maps/ww2%20map.gif">
  <img src="https://github.com/GintasS/VSOAI-D-class-project-FlatsAruodas/blob/master/maps/ww2%20map.gif" height="400" style="max-width:50%;"></img>
</a>
<blockquote>Interactive map of flats built in WW2(1939-1945).</blockquote>

## <a name="Changelog"></a>Changelog

<h3>CHANGELOG 27/03/2021</h3>
<ul>
  <li>Fixed grammar mistakes.</li>
</ul>
