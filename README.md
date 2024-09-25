# RDF Music Knowlege Graph

The project consists in the construction of an RDF Knowledge Graph with RDFLib starting from tabular data. The data is about music.

## Description

The main task is to create a RDF Knowledge Graph that follows the next points:

1. create an RDFLib Graph from data contained in CSV files,
2. integrate the data with DBpedia’s,
3. gathering information from unstructured data (Wikipedia),
4. include a small ontology and a genres taxonomy,
5. materialize inferences,
6. query the Graph

![KG](https://github.com/AlessandroGhiotto/RDF-music-knowledge-graph/blob/main/data/graph-image-example.png)

## Keywords

- Knowledge Representation and Reasoning (KRR)
- Knowlegde Graph
- RDFLib
- RDF, RDFS
- OWL, OWLRL
- SPARQL
- DBpedia
- WikipediaAPI

## CSV data

Here we can have a quick look at the two starting CSV files.

'album_list.csv':

<div style="max-width: 600px; margin: auto;">
  <table border="1" class="dataframe" style="font-size: 12px; width: 100%; text-align: center; border-collapse: collapse;">
    <thead>
      <tr>
        <th style="padding: 4px;">Number</th>
        <th style="padding: 4px;">Year</th>
        <th style="padding: 4px;">Album</th>
        <th style="padding: 4px;">Artist</th>
        <th style="padding: 4px;">Genre</th>
        <th style="padding: 4px;">Subgenre</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding: 4px;">1</td>
        <td style="padding: 4px;">1967</td>
        <td style="padding: 4px;">Sgt. Pepper's Lonely Hearts Club Band</td>
        <td style="padding: 4px;">The Beatles</td>
        <td style="padding: 4px;">Rock</td>
        <td style="padding: 4px;">Rock &amp; Roll, Psychedelic Rock</td>
      </tr>
      <tr>
        <td style="padding: 4px;">2</td>
        <td style="padding: 4px;">1966</td>
        <td style="padding: 4px;">Pet Sounds</td>
        <td style="padding: 4px;">The Beach Boys</td>
        <td style="padding: 4px;">Rock</td>
        <td style="padding: 4px;">Pop Rock, Psychedelic Rock</td>
      </tr>
      <tr>
        <td style="padding: 4px;">3</td>
        <td style="padding: 4px;">1966</td>
        <td style="padding: 4px;">Revolver</td>
        <td style="padding: 4px;">The Beatles</td>
        <td style="padding: 4px;">Rock</td>
        <td style="padding: 4px;">Psychedelic Rock, Pop Rock</td>
      </tr>
      <tr>
        <td style="padding: 4px;">4</td>
        <td style="padding: 4px;">1965</td>
        <td style="padding: 4px;">Highway 61 Revisited</td>
        <td style="padding: 4px;">Bob Dylan</td>
        <td style="padding: 4px;">Rock</td>
        <td style="padding: 4px;">Folk Rock, Blues Rock</td>
      </tr>
      <tr>
        <td style="padding: 4px;">5</td>
        <td style="padding: 4px;">1965</td>
        <td style="padding: 4px;">Rubber Soul</td>
        <td style="padding: 4px;">The Beatles</td>
        <td style="padding: 4px;">Rock, Pop</td>
        <td style="padding: 4px;">Pop Rock</td>
      </tr>
    </tbody>
  </table>
</div>

'rym_top_5000_all_time.csv':

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>Ranking</th>
      <th>Album</th>
      <th>Artist Name</th>
      <th>Release Date</th>
      <th>Genres</th>
      <th>Descriptors</th>
      <th>Average Rating</th>
      <th>Number of Ratings</th>
      <th>Number of Reviews</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1.0</td>
      <td>OK Computer</td>
      <td>Radiohead</td>
      <td>16 June 1997</td>
      <td>Alternative Rock, Art Rock</td>
      <td>melancholic, anxious, futuristic, alienation, ...</td>
      <td>4.23</td>
      <td>70,382</td>
      <td>1531</td>
    </tr>
    <tr>
      <td>2.0</td>
      <td>Wish You Were Here</td>
      <td>Pink Floyd</td>
      <td>12 September 1975</td>
      <td>Progressive Rock, Art Rock</td>
      <td>melancholic, atmospheric, progressive, male vo...</td>
      <td>4.29</td>
      <td>48,662</td>
      <td>983</td>
    </tr>
    <tr>
      <td>3.0</td>
      <td>In the Court of the Crimson King</td>
      <td>King Crimson</td>
      <td>10 October 1969</td>
      <td>Progressive Rock, Art Rock</td>
      <td>fantasy, epic, progressive, philosophical, com...</td>
      <td>4.30</td>
      <td>44,943</td>
      <td>870</td>
    </tr>
    <tr>
      <td>4.0</td>
      <td>Kid A</td>
      <td>Radiohead</td>
      <td>3 October 2000</td>
      <td>Art Rock, Experimental Rock, Electronic</td>
      <td>cold, melancholic, futuristic, atmospheric, an...</td>
      <td>4.21</td>
      <td>58,590</td>
      <td>734</td>
    </tr>
    <tr>
      <td>5.0</td>
      <td>To Pimp a Butterfly</td>
      <td>Kendrick Lamar</td>
      <td>15 March 2015</td>
      <td>Conscious Hip Hop, West Coast Hip Hop, Jazz Rap</td>
      <td>political, conscious, poetic, protest, concept...</td>
      <td>4.27</td>
      <td>44,206</td>
      <td>379</td>
    </tr>
  </tbody>
</table>
</div>
