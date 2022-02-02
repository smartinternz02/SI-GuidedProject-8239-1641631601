# SI-GuidedProject-8239-1641631601
Predicting invasive ductal carcinoma in tissue slices
Motivation
Inasive ductal carcinoma (IDC) is - with ~ 80 % of cases - one of the most common types of breast cancer. It's malicious and able to form metastases which makes it especially dangerous. Often a biopsy is done to remove small tissue samples. Then a pathologist has to decide whether a patient has IDC, another type of breast cancer or is healthy. In addition sick cells need to be located to find out how advanced the disease is and which grade should be assigned. This has to be done manually and is a time consuming process. Furthermore the decision depends on the expertise of the pathologist and his or her equipment. Therefor deep learning could be of great help to automatically detect and locate tumor tissue cells and to speed up the process. In order to exploit the full potential one could build a pipeline using massive amounts of tissue image data of various hospitals that were evaluated by different experts. This way one would be able to overcome the dependence on the pathologist which would be especially useful in regions where no experts are available .

Our goal
As we started with this analysis we asked ourselves if we would be able to improve the results that were presented 2014 in the paper Automatic detection of invasive ductal carcinoma in whole slide images with Convolutional Neural Networks of professor Anant Madabhushi and his group. Many years have passed by since then and it's very likely that all methods used in the paper have already been changed, improved and that new research has already been done. Nonetheless it's a very good exercise to practice or develop own deep learning and data science skills.

Methods presented in the paper
Collecting information... ;-)

In the paper tissue slices of 162 patients were used all having IDC (113 used for training and 49 for validation)
One pathologist was used to determine regions of IDC given a tissue slice
evaluation metric: F1 score and balanced accuracy
Our goal: Given a patient and a patch of a tissue slice predict wheather it contains IDC or not.
3 possibilities: healthy tissue, IDC, another subtype of breast cancer
business case: prediction so far is done manually by pathologists and varies from expert to expert. The goal is to assist with an automatic detection of tumors (not expert dependent).
Table of contents
What is meant by invasive ductal carcinoma?
Preparation & peek at the data structure
Loading packages and settings
Exploring the data structure
Exploratory analysis
What do we know about our data?
Looking at healthy and invasive ductal carcinoma patches
Visualising the breast tissue
Setting up the machine learning workflow
Settings
Validation strategy
Target distributions
Creating pytorch image datasets
Creating pytorch dataloaders
Defining the model structure
Setting up the loss function
Selecting an evaluation metric
Building the training loop
Searching for an optimal cyclical learning rate
Performing the training or loading results
Exploring results and errors
Loss convergence
The probability landscape of invasive ductal carcinoma
Going into details
Conclusion
What is meant by invasive ductal carcinoma? 
Lobules and ducts of the breast

This illustration created Mikael Häggström shows the anatomy of a healthy breast. One can see the lobules, the glands that can produce milk which flews through the milk ducts. Ductal carcinoma starts to develop in the ducts whereas lobular carcinoma has its origin in the lobules. Invasive carcinoma is able to leave its initial tissue compartment and can form metastases.
