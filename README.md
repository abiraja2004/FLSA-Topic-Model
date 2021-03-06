# FLSA-Topic-Model

Fuzzy Latent Semantic Analysis 

FLSA_TM is Open Source Software, and is released under the Apache License Version 2.0. You are welcome to use the code under the terms of the licence for research or commercial purposes. Please acknowledge its use with a citation:

Karami, Amir, et al. "Fuzzy Approach Topic Discovery in Health and Medical Corpora." International Journal of Fuzzy Systems (2017): 1-12.

or 

@article{karami2017fuzzy,

  title={Fuzzy Approach Topic Discovery in Health and Medical Corpora},
  
  author={Karami, Amir and Gangopadhyay, Aryya and Zhou, Bin and Kharrazi, Hadi},
  
  journal={International Journal of Fuzzy Systems},
  
  pages={1--12},
  
  publisher={Springer}
  
}





1- Data format

InputFile accepts both txt and csv format. Each line in a .txt or .csv is a document. The data is a txt or csv file where each line is of the form:

Document1

Document2

....

It is important to know that the last line should be empty. 




2- Seetings

First, Download and Install R and RStudio. 

Second, download FLSA_TM.R and open it with RStudio >  File > Open File. Select all FLSA_TM code in Source or Script and click on Run.

Third, use the following commands in RStudio Console to install the prerequisite packages: 

install.packages(tm)

install.packages(svd)

install.packages(topicmodels)

install.packages(lsa)

install.packages(topsis)

install.packages(fclust)

install.packages(devtools)

install.packages(irlba)

install.packages(skmeans)

install.packages(data.table)

install.packages(SnowballC)

install.packages(wordcloud)

install.packages(RColorBrewer)

install.packages(tictoc)

Fourth, It is suggested to create a folder to save the outputs in that folder such as "/Users/Amir/Desktop/FLSA".

Fifth, The FLSA_TM function is in the following format and all the variables should be defined:

FLSA_TM (InputFile,Num_Topics,Num_Words,WW,Destination)

InputFile: A txt or csv file that each line is a document and the last line is empty. This means that all the documents should be in one file (not seprate .txt files in a folder). Users can put the input file in the folder that just created such as InputFile="/Users/Amir/Desktop/FLSA/data.txt"

Num_Topics: Number of Topics

Num_Words: Number of Words per topic that users want to see in Top_words_per_Topics.txt file

WW: There are four Word Weighting methods in this package.(1) WW=1 is tf_idf, (2) WW=2 is tf_normal, (3) WW=3 is tf_entropy, and (4) WW=4 is tf_gw_gfidf. Users can try all these methods to see which one works for their project. 

Destination: Users need to define the destination folder such as Destination="/Users/Amir/Desktop/FLSA"

One example is 

FLSA_TM ("/Users/Amir/Desktop/FLSA/data.txt",20,10,1,"/Users/Amir/Desktop/FLSA")


FLSA_TM processing time depeneds the number of documents or the number of words.



3- Outputs

There are three files as outouts in the Destination folder:

1- Probability_of_Topics_for_Documents.txt or P(T|D)

2- Probability_of_Words_for_Topics.txt or P(W|T)

3- Top_words_per_Topics.txt to show top words per topic



If you have Questions, Comments, Problems, please send an email to karami@sc.edu. 


