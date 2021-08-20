# KG Exploration and Visualization Tool  
![KG-Exploration](images/exploration-tool.png)
## Introduction  
[![](https://drive.google.com/thumbnail?id=1nv8U7Q_r0wHVOA1qBuVeOXNruPUGUCOx)](https://drive.google.com/file/d/1nv8U7Q_r0wHVOA1qBuVeOXNruPUGUCOx/view?usp=sharing) (Click to play)

The Knowledge Graph Exploration and Visualization Tool is a full-stack web application on the top of TigerGraph services to provide an easy-to-use graphical user interface and get insights into the rich semantics in knowledge graphs. We want to build an easy search interface to discover and visualize what is in the knowledge artifacts.

The tool consists of a Flask service to communicate data with the TigerGraph and a client to render the tool with React, Redux, Axios, ReGraph, Material-UI, etc.

TigerGraph is a tool with multiple graph utilities such as definining the schema, mapping to data, visualizing mappings and querying results. It runs on a Docker image and uses a shared directory between its docker shell and your host OS.
The following instructions are based on the [TigerGraph GitHub Repo](https://github.com/tigergraph/ecosys/blob/master/demos/guru_scripts/docker/README.md) and are arranged here for your convenience.

Features in eight sections:  
- [Schema Layout](#schema-layout)
- [Semantic search](#semantic-search)
- [Graph layout](#graph-layout)
- [Filtering capabilities](#filtering-capabilities)
- [Table view](#table-view)
- [Insights](#insights)
- [Workflow](#workflow)
- [Changing Database](#changing-database)


## Features

*If the resolution is low, you can manually select higher resolution and full screen mode.*
### Schema layout
Schema layout would help you gain insight into the structure of the graphs. 
1. Select and search for a vertex type, highlight neighbors  
    [![](https://drive.google.com/thumbnail?id=1ceqlupWXHBVJbLTT4mn-LthLycKdsiR7)](https://drive.google.com/file/d/1ceqlupWXHBVJbLTT4mn-LthLycKdsiR7/view?usp=sharing) (Click to play)
2. Search for vertex types and highlight all the shortest paths between selected types  
    [![](https://drive.google.com/thumbnail?id=1BVEBl8s0vlzrHfj3tahAjA6GIR2nAAoi)](https://drive.google.com/file/d/1BVEBl8s0vlzrHfj3tahAjA6GIR2nAAoi/view?usp=sharing) (Click to play)
3. Graph layout  
    [![](https://drive.google.com/thumbnail?id=1xBgUZD1lh6PZON3W0UxGVtxRAUP3oqBt)](https://drive.google.com/file/d/1xBgUZD1lh6PZON3W0UxGVtxRAUP3oqBt/view?usp=sharing) (Click to play)
4. Hide types  
    [![](https://drive.google.com/thumbnail?id=1YdU4YoXYeTGNlsyI6wFG59nNUEs69ygn)](https://drive.google.com/file/d/1YdU4YoXYeTGNlsyI6wFG59nNUEs69ygn/view?usp=sharing) (Click to play)
5. Hovering and labeling  
    [![](https://drive.google.com/thumbnail?id=1im_8mV0R8_yTPsmFQkH9-lXW67P5anyq)](https://drive.google.com/file/d/1im_8mV0R8_yTPsmFQkH9-lXW67P5anyq/view?usp=sharing) (Click to play)
6. Switch the graphs  
    [![](https://drive.google.com/thumbnail?id=1Z_7XnsSaTvEPjUsKGFGso8fv6kdCYcxJ)](https://drive.google.com/file/d/1Z_7XnsSaTvEPjUsKGFGso8fv6kdCYcxJ/view?usp=sharing) (Click to play)


### Semantic search
Semantic search is a google-like search tool to help users discover and explore knowledge in the knowledge graph, using spaCy as an NLP engine to semantically translate English queries to GSQL interpreted queries depending on the graph schema. 
1. Search for a word  
    [![](https://drive.google.com/thumbnail?id=11AuH-cMJCyyWZFXYPUkUPC4ps02ZrtJL)](https://drive.google.com/file/d/11AuH-cMJCyyWZFXYPUkUPC4ps02ZrtJL/view?usp=sharing) (Click to play)
2. Search for a type  
    [![](https://drive.google.com/thumbnail?id=1-fcLpAN224Hc9azSiy-LivDGAzeSMBQk)](https://drive.google.com/file/d/1-fcLpAN224Hc9azSiy-LivDGAzeSMBQk/view?usp=sharing) (Click to play)
3. Semantic search for a type with keywords  
    [![](https://drive.google.com/thumbnail?id=1mgqAjdSbgs8ojxiuYEIv-8MoEb8Yh17I)](https://drive.google.com/file/d/1mgqAjdSbgs8ojxiuYEIv-8MoEb8Yh17I/view?usp=sharing) (Click to play)
4. Display the English explanation  
    [![](https://drive.google.com/thumbnail?id=16Z6lGpXw-5hIlw_y6Z3augwHKGCcCYS8)](https://drive.google.com/file/d/16Z6lGpXw-5hIlw_y6Z3augwHKGCcCYS8/view?usp=sharing) (Click to play)
5. Execute an interpreted query  
    [![](https://drive.google.com/thumbnail?id=1LRHODHT-FBNOKx73xnJfsrcQvQADfkrM)](https://drive.google.com/file/d/1LRHODHT-FBNOKx73xnJfsrcQvQADfkrM/view?usp=sharing) (Click to play)
6. Expand from a vertex  
    [![](https://drive.google.com/thumbnail?id=1fzNsaWbzmZbjEKA_PMLsIK8Gy41Xxrmx)](https://drive.google.com/file/d/1fzNsaWbzmZbjEKA_PMLsIK8Gy41Xxrmx/view?usp=sharing) (Click to play)
7. Expand with limitation  
    [![](https://drive.google.com/thumbnail?id=14BOgw40Y66eElgyvqjvUlkiHoRKqmXZt)](https://drive.google.com/file/d/14BOgw40Y66eElgyvqjvUlkiHoRKqmXZt/view?usp=sharing) (Click to play)
8. Select vertices  
    [![](https://drive.google.com/thumbnail?id=1FtZLucY1KwjflpKGt8LiFafHNt48YSZz)](https://drive.google.com/file/d/1FtZLucY1KwjflpKGt8LiFafHNt48YSZz/view?usp=sharing) (Click to play)
9. Find a shortest path and all shortest paths  
    [![](https://drive.google.com/thumbnail?id=1SRZLuYzaioFdsg0fQv_B2fOSVGyfJdfE)](https://drive.google.com/file/d/1SRZLuYzaioFdsg0fQv_B2fOSVGyfJdfE/view?usp=sharing) (Click to play)
10. Find all connections  
    [![](https://drive.google.com/thumbnail?id=1KjtIJsBYxyAMiQavWlvLwCe5aIfzTudJ)](https://drive.google.com/file/d/1KjtIJsBYxyAMiQavWlvLwCe5aIfzTudJ/view?usp=sharing) (Click to play)
11. Find paths with limitation  
    [![](https://drive.google.com/thumbnail?id=1UiH0c-nfmaNukwYc9jb6z_7PCU2VxFUs)](https://drive.google.com/file/d/1UiH0c-nfmaNukwYc9jb6z_7PCU2VxFUs/view?usp=sharing) (Click to play)
12. New search and more search  
    [![](https://drive.google.com/thumbnail?id=1ss_xg5Vc0wD9a6YbDGBMTO01DXC8dS2l)](https://drive.google.com/file/d/1ss_xg5Vc0wD9a6YbDGBMTO01DXC8dS2l/view?usp=sharing) (Click to play)
13. Reset the graph  
    [![](https://drive.google.com/thumbnail?id=1-OY03jKAyNZyiBiIiCY45YHc9BgjVbJp)](https://drive.google.com/file/d/1-OY03jKAyNZyiBiIiCY45YHc9BgjVbJp/view?usp=sharing) (Click to play)


### Graph Layout
This is to better display the search results.  
1. Highlight the neighbors and edges from selected vertices, and node style  
    [![](https://drive.google.com/thumbnail?id=1uVzySjh7IMCLec72rLMGt-zHRzazptuE)](https://drive.google.com/file/d/1uVzySjh7IMCLec72rLMGt-zHRzazptuE/view?usp=sharing) (Click to play)
2. Graph layout  
    [![](https://drive.google.com/thumbnail?id=16sFVm2BKULR879zoiSlygIduaJdqUlyI)](https://drive.google.com/file/d/16sFVm2BKULR879zoiSlygIduaJdqUlyI/view?usp=sharing) (Click to play)
3. Group vertices by types  
    [![](https://drive.google.com/thumbnail?id=1D0wOs0iZzHjsYkjrh743wrpTUCasRfBC)](https://drive.google.com/file/d/1D0wOs0iZzHjsYkjrh743wrpTUCasRfBC/view?usp=sharing) (Click to play)
4. Group the selection and group level  
    [![](https://drive.google.com/thumbnail?id=1EjnnCPY06ka0lu9Yqpqd8EHb9w4dylNX)](https://drive.google.com/file/d/1EjnnCPY06ka0lu9Yqpqd8EHb9w4dylNX/view?usp=sharing) (Click to play)
5. Download the image  
    [![](https://drive.google.com/thumbnail?id=1ZZw9WdYx9DRVD_LiYPX51q0TaNNj_euE)](https://drive.google.com/file/d/1ZZw9WdYx9DRVD_LiYPX51q0TaNNj_euE/view?usp=sharing) (Click to play)


### Filtering capabilities
This is to help users filter and extract useful information from search results. 
1. Hide types  
    [![](https://drive.google.com/thumbnail?id=1tw2tKEI3dZf3UIrqaVBhTBnCs_AnOvZA)](https://drive.google.com/file/d/1tw2tKEI3dZf3UIrqaVBhTBnCs_AnOvZA/view?usp=sharing) (Click to play)
2. Hide selection and show selection  
    [![](https://drive.google.com/thumbnail?id=15eeTaOz_j7hhdJrV_DuNy6JS2UNXtOLT)](https://drive.google.com/file/d/15eeTaOz_j7hhdJrV_DuNy6JS2UNXtOLT/view?usp=sharing) (Click to play)
3. Vertex label  
    [![](https://drive.google.com/thumbnail?id=1EAzrdcz_Lf1ztNH5UYWhu7-vApGvfNf8)](https://drive.google.com/file/d/1EAzrdcz_Lf1ztNH5UYWhu7-vApGvfNf8/view?usp=sharing) (Click to play)
4. Locate vertex  
    [![](https://drive.google.com/thumbnail?id=15wFru-pHMlctxc74Ks6jLlAEpD85Bu4j)](https://drive.google.com/file/d/15wFru-pHMlctxc74Ks6jLlAEpD85Bu4j/view?usp=sharing) (Click to play)


### Table view
Table panel provides a traditional table view grouped by type of vertices. 
1. Table view and select vertices  
    [![](https://drive.google.com/thumbnail?id=1huUR7WzKRqkm45PP0qQZk0UY7E6swwgw)](https://drive.google.com/file/d/1huUR7WzKRqkm45PP0qQZk0UY7E6swwgw/view?usp=sharing) (Click to play)
2. Sort attributes, page and hide vertices  
    [![](https://drive.google.com/thumbnail?id=1j9qEcONIl5HumG15Dk_19hxHcTOiM89b)](https://drive.google.com/file/d/1j9qEcONIl5HumG15Dk_19hxHcTOiM89b/view?usp=sharing) (Click to play)


### Insights
The insight panel is to show the statistics of the graph and customized search algorithms.
1. Display the statistics of graphs  
    [![](https://drive.google.com/thumbnail?id=1D8RsM-tzuyqrb_BaWs8x1pL--IOZW-kO)](https://drive.google.com/file/d/1D8RsM-tzuyqrb_BaWs8x1pL--IOZW-kO/view?usp=sharing) (Click to play)
2. Customized search for vertices and path exploration  
    [![](https://drive.google.com/thumbnail?id=111VJPdW5xPBTGFTptN9Re_IhUjTRThTv)](https://drive.google.com/file/d/111VJPdW5xPBTGFTptN9Re_IhUjTRThTv/view?usp=sharing) (Click to play)


### Workflow
The workflow helps users undo changes, store states, and step through recording to restore data.
1. Undo and redo  
    [![](https://drive.google.com/thumbnail?id=1wzkr3nx25n_c_udOVot8wKLGqtAu4diG)](https://drive.google.com/file/d/1wzkr3nx25n_c_udOVot8wKLGqtAu4diG/view?usp=sharing) (Click to play)
2. Save recording and restore recording  
    [![](https://drive.google.com/thumbnail?id=1YD9szU-sYvFVUzGxmlUq2UNjyeuwrPnK)](https://drive.google.com/file/d/1YD9szU-sYvFVUzGxmlUq2UNjyeuwrPnK/view?usp=sharing) (Click to play)
3. Start recording and stop recording  
    [![](https://drive.google.com/thumbnail?id=15L-mLdIV3nCKBRGbo2EnmCOQNzg1zVZz)](https://drive.google.com/file/d/15L-mLdIV3nCKBRGbo2EnmCOQNzg1zVZz/view?usp=sharing) (Click to play)
4. Restore recording and replay steps  
    [![](https://drive.google.com/thumbnail?id=1M7Ldy_kJgNUpzZhOTCJC9Qhm43dT0Wa6)](https://drive.google.com/file/d/1M7Ldy_kJgNUpzZhOTCJC9Qhm43dT0Wa6/view?usp=sharing) (Click to play)
5. Delete recording and download search results  
    [![](https://drive.google.com/thumbnail?id=1Vz2_bM8uvenN9ojj1amfGiGX6MdhwN5U)](https://drive.google.com/file/d/1Vz2_bM8uvenN9ojj1amfGiGX6MdhwN5U/view?usp=sharing) (Click to play)
6. Download and upload workflow file  
    [![](https://drive.google.com/thumbnail?id=1oIKR1T2USiSkSsM39oZq2qf4e_yBAMQ_)](https://drive.google.com/file/d/1oIKR1T2USiSkSsM39oZq2qf4e_yBAMQ_/view?usp=sharing) (Click to play)


### Changing Database
This tool provides the capabilities to create, update, and delete data in the database. 
1. Create vertex and edit vertex  
    [![](https://drive.google.com/thumbnail?id=1R7fcupMP05iKLISHZ2s4LnawCw5ULdmc)](https://drive.google.com/file/d/1R7fcupMP05iKLISHZ2s4LnawCw5ULdmc/view?usp=sharing) (Click to play)
2. Create edge and edit edge  
    [![](https://drive.google.com/thumbnail?id=17yFb4JuibYEdg51s0cfPO9ajW3E2_3aH)](https://drive.google.com/file/d/17yFb4JuibYEdg51s0cfPO9ajW3E2_3aH/view?usp=sharing) (Click to play)
3. Delete vertex and delete edge  
    [![](https://drive.google.com/thumbnail?id=1gV_JkJ5ePBP0kz_zJ1f2BkAnQxKhbGxw)](https://drive.google.com/file/d/1gV_JkJ5ePBP0kz_zJ1f2BkAnQxKhbGxw/view?usp=sharing) (Click to play)
4. Undo/redo and submit  
    [![](https://drive.google.com/thumbnail?id=1FFxDnAwNPFcZokbwJ867MQXlgcYfLTm5)](https://drive.google.com/file/d/1FFxDnAwNPFcZokbwJ867MQXlgcYfLTm5/view?usp=sharing) (Click to play)
