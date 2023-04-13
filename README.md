9)..Perform the linear regression on the given data warehouse data.
Code:
x <- c(151, 174, 138, 186, 128, 136, 179, 163, 152, 131)
y <- c(63, 81, 56, 91, 47, 57, 76, 72, 62, 48)
relation<- lm(y~x)
a <- data.frame(x = 170)
result<- predict(relation,a)
print(result)
png(file = "linearregression.png")
plot(y,x,col = "blue",main = "Height & Weight Regression",
 abline(lm(x~y)),cex = 1.3,pch = 16,xlab = "Weight in Kg",ylab = "Height in 
cm")
dev.off()

8)..Perform the data clustering using clustering algorithm.
Code:
newiris<- iris
newiris$Species<-NULL
(kc<- kmeans(newiris,3))
print(kc)
table(iris$Species,kc$cluster)
plot(newiris[c("Sepal.Length","Sepal.Width")],col=kc$cluster)
points(kc$centers[,c("Sepal.Length","Sepal.Width")],col=1:3,pch=8,cex=2)


