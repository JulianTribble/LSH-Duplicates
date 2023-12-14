# LSH-Duplicates
Detecting Duplicate TV's using Minhash, LSH and clustering

Files in Repository:
Main_file.py -> Main Script with full implementation
Results_current_parameters.xlsx -> The output of the mainfile in excel form using current parameters

# Guide to using Main_file.py

After downloading all packages there is a part of the code called: "Control Room". Here you certain key aspects can be turned on and off.

Controls:
"graph_creation" setting this to True will make the code provide graphs for its output
"save_results" setting this to True will cause the code to save both an excel file of the output and the graphs
"Grid_search_on" setting this to True will cause the code to run the grid search, NOTE: when turning on the gridsearch the normal code will not run. Gridsearch is for hyperparameter optimization.

Parameters for normal running:

"n_values" Chaging this array will change the permutations that are run by the code

"max_counts" Max count regards the upper threshold for word removal. Thus all words that appear more than the max_count in the vocabulary will be removed from all titles.

"weights_on_off" setting this to True will make the code implement weights to the infrequent words that are added to the model words

"also_weights_on_brands" setting this to True will make the code implement wieghts to the identified brands that it adds to the model words.

"regex_functions" here the regex functions can be changed by implementing different regex functions

"word_weight" this changes the weight applied to the words, which words are weighted depends on the parameters: "weights_on_off" and "also_weights_on_brands"

"epsilon" this is the threshold for the clustering algorithm. Putting it lower means clustering becomes more selective whilst putting it higher does the oppposite.

"min_count" for words under this threshold are removed.

Gridsearch values parameters:

"max_counts_grid" change the array values to test which value of max_counts is optimal

"weights_on_off_grid" tests whether it is optimal to add weights to infrequent words

"also_weights_on_brands_grid" tests wheter it is optimal to add weights to brands

"regex_functions_grids" here you can add various regex functions to test their performance

# Code structure

The code is seprated into destinct parts. I will now run through each part.

1. Packages : self xplanatory, downloads the packages

2. Control Room : As mentioned earlier this is where you can change parameters and turn off and on certain aspects

3. Loading data : Data is loaded in (a json file) and converted to a data frame

4. Functions Cleaning : Functions here are used to clean the dataset. This includes standardization, cleaning of text, identfying and extracting brands from titles, extracting brands, creation of a vocabulary, title reduction. Finally a function that can be run to apply all the cleaning steps.

5. 

6. 
