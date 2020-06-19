## Load model

with open('baseline_model.pkl','rb') as f:
  model = pickle.load(f)
  
## To make predications with encoded dataset

features = ['acousticness','danceability','duration_ms','energy','explicit','instrumentalness','key','liveness','loudness','mode','popularity','speechiness','tempo','valence','year','artists_encoded',]

dennis = df[features].iloc[:1]

output = model.kneighbors(dennis)

output[1]
