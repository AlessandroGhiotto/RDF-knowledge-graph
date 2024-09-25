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

## CSV data

'album_list.csv':

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Number</th>
      <th>Year</th>
      <th>Album</th>
      <th>Artist</th>
      <th>Genre</th>
      <th>Subgenre</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>1967</td>
      <td>Sgt. Pepper's Lonely Hearts Club Band</td>
      <td>The Beatles</td>
      <td>Rock</td>
      <td>Rock &amp; Roll, Psychedelic Rock</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1966</td>
      <td>Pet Sounds</td>
      <td>The Beach Boys</td>
      <td>Rock</td>
      <td>Pop Rock, Psychedelic Rock</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1966</td>
      <td>Revolver</td>
      <td>The Beatles</td>
      <td>Rock</td>
      <td>Psychedelic Rock, Pop Rock</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1965</td>
      <td>Highway 61 Revisited</td>
      <td>Bob Dylan</td>
      <td>Rock</td>
      <td>Folk Rock, Blues Rock</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>1965</td>
      <td>Rubber Soul</td>
      <td>The Beatles</td>
      <td>Rock, Pop</td>
      <td>Pop Rock</td>
    </tr>
  </tbody>
</table>
</div>

'rym_top_5000_all_time.csv':

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
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
      <th>0</th>
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
      <th>1</th>
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
      <th>2</th>
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
      <th>3</th>
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
      <th>4</th>
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

### Keywords

- Knowledge Representation and Reasoning (KRR)
- Knowlegde Graph
- RDFLib
- RDF, RDFS
- OWL, OWLRL
- SPARQL
- DBpedia
- WikipediaAPI
