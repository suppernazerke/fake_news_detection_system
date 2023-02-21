# fake_news_detection_system
Links:
Youtube: https://youtu.be/a1FdHg9rmwM


Introduction

•	Problem

The growing prevalence of fake news on the internet poses a huge risk to individuals, businesses, and society. These erroneous or misleading facts can have a negative impact on public opinion, decision-making, and general faith in the media and institutions. Especially nowadays when there is a big political war happening in the world, fake news can be detrimental for nations. Traditional techniques of detecting and combating false news rely on human fact-checkers and information literacy of people, which may be time-consuming and subjective. The challenge is to create a Deep Learning system capable of detecting this fake news. 
False or misleading information transmitted through conventional and digital media is referred to as fake news. In recent years, since social media and the internet have made it simple for fake news to spread fast and reach a broad audience, this situation has become a major worry.  

•	Literature review

There are numerous techniques to developing an AI-powered false news detector. One approach is to analyze photos and movies using computer vision. This may entail evaluating the content of photos as well as the information linked with them to detect trends suggestive of false news. For example, an AI system may be able to determine whether a picture has been modified. https://business.adobe.com/blog/the-latest/spotting-image-manipulation-ai 
Another way is to employ the knowledge representation technique, which allows the AI system to be trained to comprehend the context and background of the text/image. This allows the AI to be trained to grasp the event, person, place, and other things referenced in the text/image, allowing it to determine whether the news is accurate. https://www.logically.ai 
Another option is to examine the text of a news item using natural language processing (NLP) tools. Analyzing the syntax, vocabulary, and general structure of the text to uncover patterns suggestive of false news might be part of this process. The system may then be trained to detect these patterns and generate predictions about the reliability of a news article using machine learning methods. https://www.thefactual.com 

•	Current work

In this project work I will create Deep Learning model to detect if the news if fake or not. It will use neural networks to model complex patterns in data that will classify news articles as real or fake. For the data sorting and training-testing, a CSV file will be loaded and processed. Then tokenization will be applied. In the end detection model will be evaluated and tested. 

•	Data Analysis
For my project I used already collected dataset from https://www.geeksforgeeks.org/fake-news-detection-model-using-tensorflow-in-python/ called data_news.csv. This csv file contains of 4 columns: Unnamed, Title, Text, Label. First column contains some numbers which we will drop in our code, and the last one “Label” shows if the news is true or false. We will change it to Boolean 0 and 1 later in my code. The number of Fake and Real news is approximately the same. Totally there is 6335 texts in the dataset. 

  

•	ML model
I initialized my model as an instance of a sequential class. Then one by one added layers to my model. First, I used embedding layer. Embedding layer converts each word into a fixed length vector of defined size. Then I added Dropout layer that will regularize my model. It will drop 20% of dataset to avoid overfitting. Convolutional 1D applies sliding convolutional filters to 1 dimensional inputs. Max Pooling 1D divides the input into pooling regions in my case with pool size 4 and then computes the maximum of each region. Next added the LTM layer makes additive interactions, that can help improve gradient flow over long sequences during training. In the final stage I used Dense layer. It will change the dimensionality of the output from the preceding layer. Model was compiled using Adam optimizer, as it is most efficient one in this case.

 

•	Results
I created an input field to enter news texts. I took real news from CNN official website https://edition.cnn.com/travel/article/venice-canal-drought-italy-climate-scli-intl/index.html and the model labeled them as true. Other fake news I gained from special website with fake news https://library-nd.libguides.com/fakenews/examples. The model defined them as fake. The last picture shows the fault of my model. The real news was shown as fake.
       



•	Discussion
Critical review of results.
The graphs above show that my model is not perfect. There is a significant gap between training and validation accuracy. Also, validation loss is increasing over number of epochs. These are the signs of overfitting, however in practice the model showed good results. However, the news about earthquakes in Turkey was defined as fake. It could have happened because the training dataset is not up to date. As years go by, the style of writing news, the news itself are changing. So, it becomes harder for Machine Learning model differentiate fake and real news.

Next Steps
The next steps of my project:
o	Develop more efficient model. 
o	Tackle the problem of overfitting.
o	Create new up-to-date dataset.
o	Make convenient website for users to insert texts.

•	Sources
https://business.adobe.com/blog/the-latest/spotting-image-manipulation-ai 
https://www.logically.ai
https://www.thefactual.com 
https://www.geeksforgeeks.org/fake-news-detection-model-using-tensorflow-in-python/
https://edition.cnn.com/travel/article/venice-canal-drought-italy-climate-scli-intl/index.html
https://library-nd.libguides.com/fakenews/examples


