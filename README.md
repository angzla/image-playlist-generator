# image-playlist-generator
TLDR; generates a playlist in Spotify based on image, using CNN trained model on the CIFAR-10 dataset. 

# Results: 
Uses a CNN image model with >60% accuracy trained on CIFAR-10 dataset that ouputs 10 possible classes: 'plane', 'car', 'bird', 'cat', 'deer', 'dog', 'frog', 'horse', 'ship', 'truck'. Using Spotify APIs and Hugging Face's crossencode genre-picker, inputs image result to find other playlists on Spotify with the same text, and averages similar features (genre, danceability, energy, key, etc.) from songs in existing playlists to create a new playlist.  

# To Run: 

Download notebook, run second model, and download crossencoder pkl (change path in your code) and create your own Spotify project (replace api key).  

# References
- First image model following this article: https://medium.com/bitgrit-data-science-publication/building-an-image-classification-model-with-pytorch-from-scratch-f10452073212
- Second image model uses similar techniques as this notebook but edited to work with CIFAR-10 instead of numbers: https://www.kaggle.com/code/juiyangchang/cnn-with-pytorch-0-995-accuracy/notebook
- Playlist generator follows this article, changes format of arguments and organization of functions: https://medium.com/@doron.reiffman/moodika-generating-spotify-playlists-based-on-free-text-input-8f4eccc1254
