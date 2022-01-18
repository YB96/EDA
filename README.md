# EDA on Brazilian E-Commerce Olist
![](https://imgur.com/ba6nzDC.png)

## Introduction
This is a Brazilian ecommerce public dataset of orders made at [Olist Store]((https://olist.com/pt-br/)). The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers. It has also been included a geolocation dataset that relates Brazilian zip codes to lat/lng coordinates.

Olist is a Brazilian departmental store (marketplace) that operates in e-commerce segment, but is not an e-commerce itself. It operates as a SaaS (Software as a Service) technology company since 2015. It offers a marketplace solution (of e-commerce segment) to shopkeepers of all sizes (and for most segments) to increase their sales whether they have online presence or not.
## Installing libraries and dataset
### Downloading required libraries.
`Run this cell on terminal or on any notebook`.<br>
!pip install jovian opendatasets plotly wordcloud folium matplotlib seaborn --upgrade --q <br>
`Importing required libraries` <br>
import jovian <br>
import opendatasets as od <br>
import os <br>
import pandas as pd <br>
from wordcloud import WordCloud <br>
import plotly.express as px <br>
import plotly.graph_objects as go <br>
from plotly.subplots import make_subplots <br>
import matplotlib.pyplot as plt <br>
import seaborn as sns  <br>
import folium
from folium.plugins import FastMarkerCluster, HeatMap <br>

### Downloading dataset
dataset_url ='https://www.kaggle.com/olistbr/brazilian-ecommerce' <br>
`You need to provide your kaggle credentials` <br>
od.download(dataset_url) <br>

