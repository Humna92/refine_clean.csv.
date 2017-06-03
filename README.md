
#age
titanic$age[is.na(titanic$age)]=mean(titanic$age, na.rm = TRUE)
View(titanic)
#Lifeboat
titanic <- within(titanic,Lifeboat<-ifelse(boat=="NA",0,1))
titanic$Lifeboat[is.na(titanic$Lifeboat)]=0
#cabin
titanic <-within(titanic, has_cabin_number<-ifelse(cabin=="NA",0,1))
titanic$has_cabin_number[is.na(titanic$has_cabin_number)]=0
