# Statistical-Analysis-MScA-31007-Assignment-6
Analyze The Training Sample, Unscramble The Main Sample Using The Classifier Trained On The Training Sample

## Assignment 

#### Download your sample from left sidebar, unpack and read it.

#### Create variable dataPath equal to path to your local folder where you saved the data files Week6_Test_Sample_Train.csv and Week6_Test_Sample_Test.csv.
It should look like:

dataPath<-"C:/Your path"
Note that in R path is specified with forward slash “/”. Do not end the path with / when you assign dataPath.

#### Read the data training and the main sample. .

train_dat <- read.table(paste(dataPath,'Week6_Test_Sample_Train.csv',sep = '/'), header=TRUE)

main_dat <- read.table(paste(dataPath,'Week6_Test_Sample_Test.csv',sep = '/'), header=TRUE)

#### The training sample train_dat has the following format:

train_dat$Output - output Y values;
train_dat$Input - predictor X values;
train_dat$Selection.Sequence - vector of 0 and 1.

#### The main sample main.dat has the following format:

main_dat$Output - output Y values;
main_dat$Input - predictor X values;
#### Analize the training sample as you did in Sections 1.1 and 1.2. Unscramble the main sample using the classifier trained on the training sample (Section 1.3). Create variable Unscrambling.Sequence.Logistic using the same method as you did in Section 1.3 and save it in file result.csv.

#### Create list variable res

res <- list(Unscrambling.Sequence.Logistic =  Unscrambling.Sequence.Logistic)
Save res to a file and upload the file using left sidebar.

write.table(res, file = paste(dataPath,'result.csv',sep = '/'), row.names = F)

#### Your score will be equal to balanced accuracy of matching the correctly estimated selection sequence.
