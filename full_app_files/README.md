# Full Interactive App Files

Our app was developed and tested using pre-processed reviews obtained from the authors of "Online App Review Analysis for Identifying Emerging Issues" (see main repository for full citation). A demo video using all reviews can be seen on the project website (https://goldenmonster0602.github.io/w210final.github.io/). In the 'ios' and 'android' apps, there are folders for each app included in the paper. The total_info.txt contains the review data that is used for training and app visualization. In consideration of the authors who graciously provided us with the data, only the first 10 reviews for each app have been uploaded, so the code will not actually replicate the application in the demo video, which used over 160,000 reviews total. However, the application can still be used on review data processed and formatted in the same way.


**load_and_save_gui_data.py**

For each app, this script will load review data from text files, train a Word2Vec model on them, and save the model - as well as the reviews in a data frame with other relevant data - into a location outside of the repository. This must be run before running the main application.

**gui.py**

After the Word2Vec model files and reviews have been saved, the app can be run using a bokeh server (*bokeh serve gui.py*).
