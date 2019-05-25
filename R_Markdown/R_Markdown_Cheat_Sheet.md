---
title: "R Markdown Cheat Sheet"
author: "Milca Tarshish"
date: "5/24/2019"
output: 
  html_document:
    keep_md: true
---

## New line:   
put 2 spaces at the end of the line  

## Text styles:
*\*italic\**  
**\*\*bold\*\***  
***\*\*\*italic and bold\*\*\****   
^^superscript^^ regular   
~\~subscript\~~ regular


# # First Heading  
## ## Second Heading
### ### Third Heading
#### #### Forth Heading 
##### ##### Fifth Heading
###### ###### Sixth Heading  
Regular text size  

## How to color part of the text:  
Add the following function to your markdown doc (with Echo=F):  

```r
format_with_col = function(x, color){
  if(knitr::is_latex_output())
    paste("\\textcolor{",color,"}{",x,"}",sep="")
  else if(knitr::is_html_output())
    paste("<font color='",color,"'>",x,"</font>",sep="")
  else
    x
}
```
And then whenver need text in specific color just do as following examples (again - with echo=F):  

```r
red_text<-format_with_col("text to print in red", "red")
green_text<-format_with_col("want to print this in green", "green4")
```
<font color='red'>text to print in red</font> regular black text <font color='green4'>want to print this in green</font>   


## Unordered Lists
\- item 1  
\- item 2  
\- item 3  

## Ordered Lists
1. item 1  
2. item 2  
3. item 3  

## url links:   
![put here the text to click on, for example "for more details click here"] (put here the correct url)   
or, for advanced links you can do the following:  
![text to ckick on 1]![1]  
![text to ckick on 2]![2]    
![text to ckick on 3]![3]   
and then (somewhere in the doc):  
![1]:url 1  
![2]:url 2  
![3]:url 3  

## R code as part of Rmarkdown doc:  
\`\`\`\{r}  
put you R code here  
\`\`\`  

You can ident your R code sections by:  
\`\`\`\{r name_1}  
put you R code here  
\`\`\`  

## using Embedded R code variables as part of text:  
Example: 


```r
array2<-c(1,2,3,4)
var2<- sum(array2)  
```

![](C:\coursera\myDocs\image1.PNG)  

## options in R code chunks:   
1. cache: cache results for future knits (default = FALSE)  
2. echo: Display code in output document (default = TRUE)  
3. fig.cap: plot caption as character string (default = NULL)  
4. fig.height: height of plot in inches.   
5. fig.width: width of plot in inches.  
6. message: display code messages in document (default = TRUE).  
7. results:  
7.1 'asis' - passthrough results (not in a special box, but more apearing like part of the text)  
7.2 'hide' - do not display results  
7.3 'hold' - put all results below all code  
        (default = 'markup')  
8. warning: display code warnings in document (default = TRUE).  

Example for using these options: 

\`\`\`{r results="asis",message=FALSE}  
x<-1    
\`\`\`  

## R Mardown Cheat Sheet from the web: 
[R markdown cheat Sheet from the web](https://www.rstudio.com/wp-content/uploads/2016/03/rmarkdown-cheatsheet-2.0.pdf)
