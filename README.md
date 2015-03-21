# datacourse
Files related to the coursera data course
#Downloading files from the tutorial
dataset_url <- "http://s3.amazonaws.com/practice_assignment/diet_data.zip"
download.file(dataset_url, "diet_data.zip")
unzip("diet_data.zip", exdir = "diet_data")

#looping
dat <- data.frame()
for (i in 1:5){
  dat <- rbind(dat,read.csv(files_full[i]))
}
median(dat$Weight,na.rm=TRUE)

dat_30 <- dat[which(dat[,"Day"]==30),]
