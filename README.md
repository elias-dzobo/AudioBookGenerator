# AudioBookGenerator
a program that can either read text from an image or text file, summarize it using a transformer and create an audiobook. This was inspired by my desire as a student to be able to listen to lecture note summaries in my spare time.

# Design Details 
The system takes two forms of input date, image data and text data
Based on the data taken in
- image data -> text is extracted from image -> text is summarized -> summary is stored -> text is used to generate audiofile -> audiofile is also stored

- text data -> api call to transfromer -> text is summarized -> summary is stored -> audiofile is generated -> audiofile is stored

# IMAGE DATA
a. If the data is an image data, a call to pythons pyteseract module is initiated to capture the text from the image data 
b. Once the text is captured, a call to hugging face transformer API is made to summarize the text 
c. The summarized text is noted and an audiofile is created from summarized text.

# TEXT DATA
a. An API call to the hugging face trasnformer is initaited 
b. The content of the text file is summarized and stored
c. An audiofile is created from the summarized text and stored.
