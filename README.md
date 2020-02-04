# Lab5

Turn in one copy for each group. If group members are not present in class they will be required to complete their own lab to receive credit. Please turn in **both a DOC or PDF file and your R Markdown script**.  

## Lab Overview



## Questions
Answer the following questions in this R Markdown document. Please include code where necessary.

### 1. Central Limit Theorem Example (10 points)

The central limit theorem is a foundational idea in statistical inference. Typically, it is assumed that the mean of a sample converges to a normal distribution when the sample size is greater than (20 or 30?). So where do these numbers come from? 

To look at this question, modify the function to also print a histrogram. For full credit your function should have appropriate titles, labels, and be aesthetically pleasing.

```
CLT <- function(num.sims){
  # function that simulates uniform random numbers to illustrate the central limit theorem
  # ARGS: num.sims - the number of samples to average in central limit theorem
  # RETURNS: list containing the mean and standard deviation of the average of the samples
  #          SHOULD ALSO CREATE A HISTOGRAM, WITH APPROPRIATE TITLES
  num.replicates <- 10000 # how many times to repeat this process
  samples <- rep(0, num.replicates)
  for (i in 1:num.replicates){
    samples[i] <- mean(runif(num.sims, min = 0, max = 100))
  }
  # CREATE HISTOGRAM HERE
  return(list(mean(samples), sd(samples)))
}
```


Demonstrate the function works by calling the function with 10, 30, 100, and 1000 samples. Briefly discuss the differences in these figures/results.

### 2. (10 points)

Download the data set on earthquakes, provided by the USGS, available at [http://www.math.montana.edu/ahoegh/teaching/stat408/datasets/EarthquakesAll.csv](http://www.math.montana.edu/ahoegh/teaching/stat408/datasets/EarthquakesAll.csv). The data set contains earthquakes from 1965 to 2016.

Create a compelling graphic from this data set. The choice of what and how is completely up to you. Then provide a short summary of the story your graphic depicts.
