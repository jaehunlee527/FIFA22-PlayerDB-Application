# [Streamlit] FIFA22 Player Search Engine

Searching players can be cumbersome on FIFA22. I wanted to be able to find talents faster and easier, so I decided to create an app that caters to my (and preferably to other FIFA users') needs. The app provides two functionalities:

### 1) Search players by filtering
  - Select ranges of age, market value, player country, league and positions to find players with top qualities that users are looking for.
### 2) Look up particular player 
  - Search a particular player and see basic information including the player's top traits. Also, see list of players with similar traits. 
  
The Streamlit App can be accessed [here](https://share.streamlit.io/jayhoneylee527/fifa22-playerdb/main/fifa.py).

&nbsp;
<p align="center">
  <img src="images/messi_dash.PNG" width="600" height="400">
</p>

### Data Source
players_22.csv has been downloaded from [Kaggle](https://www.kaggle.com/stefanoleone992/fifa-22-complete-player-dataset?select=players_22.csv).

### How are the players of "similar traits" selected?

Based on 36 traits of each player, PCA reduces the trait dimensions down to 15. (~98% explained variance)
Then, using Euclidean distance, the app prints out players of the minimum distances in the ascending order. 
