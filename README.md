# - IMDB-Movie-Recommendations-Year-Predictions
Simple architecture consisting of the base of the VGG16 pre-trained model, which produces embeddings of the input image (movie poster), followed by a fully-connected head which performs regression and estimates the year of the input movie.

# Part 1. Create embedding 
Use a pretrained model, eg as provided by Keras, to create a flat (ie 1D) embedding vector of some size embedding_size for each movie poster, and put all of these together into a single tensor of shape (n_movies, embedding_size).

# Part 2. Define a nearest-neighbour function 
Write a function def nearest(img, k) which accepts an image img, and returns the k movies in the dataset whose posters are most similar to img (as measured in the embedding), ranked by similarity.

# Part 3: Demonstrate your nearest-neighbour function
Choose any movie poster. Call this the query poster. Show it, and use your nearest-neighbour function to show the 3 nearest neighbours (excluding the query itself). This means call the function you defined above.
Write a comment: in what ways are they similar or dissimilar? Do you agree with the choice and the ranking? Why do you think they are close in the embedding? Do you notice, for example, that the nearest neighbours are from a similar era?

# Part 4: Year regression 
Let's investigate the last question ("similar era") above by running regression on the year, ie attempt to predict the year, given the poster. Use a train-test split. Build a suitable Keras neural network model for this, as a regression head on top of the embedding from Part 1. Include comments to explain the purpose of each part of the model. It should be possible to make a prediction, given a new poster (not part of the original dataset). Write a short comment on model performance: is it possible to predict the year? Based on this result, are there trends over time?

# Part 5: Improvements 
Propose a possible improvement. Some ideas are suggested below. The chosen improvement must be notified to the lecturer at least 1 week before submission and must be approved by the lecturer to avoid duplication with other students. Compare the performance between your original and your new model (the proposed improvement might not actually improve on model performance -- that is ok). Some marks will be awarded for more interesting / challenging / novel improvements.

