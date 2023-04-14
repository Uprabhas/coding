9)..Perform the linear regression on the given data warehouse data.
Code:
1. x <- c(151, 174, 138, 186, 128, 136, 179, 163, 152, 131)
2. y <- c(63, 81, 56, 91, 47, 57, 76, 72, 62, 48)
3. relation<- lm(y~x)
4. a <- data.frame(x = 170)
5. result<- predict(relation,a)
6. print(result)
7. png(file = "linearregression.png")
8. plot(y,x,col = "blue",main = "Height & Weight Regression", abline(lm(x~y)),cex = 1.3,pch = 16,xlab = "Weight in Kg",ylab = "Height in cm")
9. dev.off()

8)..Perform the data clustering using clustering algorithm.
Code:
1. newiris<- iris
2. newiris$Species<-NULL
3. (kc<- kmeans(newiris,3))
4. print(kc)
5. table(iris$Species,kc$cluster)
6. plot(newiris[c("Sepal.Length","Sepal.Width")],col=kc$cluster)
7. points(kc$centers[,c("Sepal.Length","Sepal.Width")],col=1:3,pch=8,cex=2)


