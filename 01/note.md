<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/01
Author: 	shumez <https://github.com/shumez>
Created: 	2019-05-30 18:19:8
Modified: 	2019-06-01 14:37:25
-----
Copyright (c) 2019 shumez
-->

# [01. Introduction]

## Contents

* [01.01. Who Should Read This Book?][0101]
* [01.02. Historical Trends in Deep Learning][0102]
	* [01.02.01. The Many Names and Changing Fortunes of Neural Networks][010201]
	* [01.02.02. Increasing Dataset Sizes][010202]
	* [01.02.03. INcreasing Model Sizes][010203]
	* [01.02.04. Increasing Accuracy, Complexity and Real-World Impact][010204]

##

ancient Greece

* Galatea by Pygmalion
* Talos by Daedalus
* Pandora by Hephaestus

**AI**

**deep learning**

**logistic regression**

**naive Bayes**

## 01.01. Who Should Read This Book?

## 01.02. Historical Trends in Deep Learning

### 01.02.01. The Many Names and Changing Fortunes of Neural Networks

* **cybernetics** in 1940s-1960s
* **connectionism** in 1980s-1990s
* deep learning in 2006

<iframe name="ngram_chart" src="https://books.google.com/ngrams/interactive_chart?content=cybernetics%2Cconnectionism%2Cneural+network%2Cdeep+learning%2Cmachine+learning&year_start=1945&year_end=2019&corpus=15&smoothing=3&share=&direct_url=t1%3B%2Ccybernetics%3B%2Cc0%3B.t1%3B%2Cconnectionism%3B%2Cc0%3B.t1%3B%2Cneural%20network%3B%2Cc0%3B.t1%3B%2Cdeep%20learning%3B%2Cc0%3B.t1%3B%2Cmachine%20learning%3B%2Cc0" width=800 height=300 marginwidth=0 marginheight=0 hspace=0 vspace=0 frameborder=0 scrolling=no></iframe>

**artificial neural networks** (ANNs)

\(f(\mathbf{x}, \mathbf{w}) = x_1 x_1 + \cdots + x_n w_n\)

**McCulloch-Pitts Neuron** ([McCulloch, Pitts, 1943][1943_Pitts_McCulloch])

perceptron ([Rosenblatt, 1958][1958_Rosenblatt], [1962][1962_Rosenblatt])

ADALINE ([Widrow, Hoff, 1960][1960_Hoff_Widrow])

**stochasic gradient descent**

**linear models**

limitation:  
connot learn the XOR fn  
\[
	\begin{cases}
		f([0,1], \mathbf{w}) = 1 \\
		f([1,0], \mathbf{w}) = 1 \\
		f([1,1], \mathbf{w}) = 1 \\
		f([0,0], \mathbf{w}) = 0 
	\end{cases}
\]

[Minsky, Papert, 1969][1969_Papert_Minsky]

[Olshausen, Field, 2005][2005_Field_Olshausen]


ferrets brain ([Von Melshner, 2000][2000_VonMekshner])

Neocognitron ([Fukushima, 1980][1980_Fukushima]) &rarr; modern convolutional network ([LeCun, 1998][1998_KeCun])

**rectified linear unit**

original Cognitron ([Fukushima, 1975][1975_Fukushima])

[Nair, Hinton, 2010][2010_Hinton_Nair], [Glorot, 2011][2011_Glorot] citing neuroscience, [Jarrett, 2009][2009_Jarrett] citing more engineering-oriented


1980s: second wave of NN

movement **connectionism** / **parallel distributed processing** ([Rumelhart, 1986][1986_Rumelhart], [McClelland, 1995][1995_McClelland])

models of cognition grounded in neural implementation ([Touretzky, Minton, 1985][1985_Minton_Touretzky]), reviving work og Fonald Hebb in 1940s ([Hebb, 1949][1949_Hebb])

connectionsim: large num of sumple computational units can ahchive intelligent behavior

**distributed representation** ([Hinton, 1986][1986_Hinton])  
e.g., 3 neurons describing 3 colors & 3 neurons 3 objects

**back-propagation** ([Rumelhart, 1986][1986_Rumelhart], [LeCun, 1987][1987_LeCun])

during 1990s  
[Hochreiter, 1991][1991_Hochreiter], [Bengio, 1994][1994_Bengio]

Long short-term memody (LSTM) ([Hochreiter, Schmidhuber, 1997][1997_Schmidhuber_Hochreiter])

mid-1990s  
Kernel machines ([Boser, 1992][1992_Boser], [Corters, Vapnik, 1995][1995_Vapnik_Cortes], [Schölkopf, 1999][1999_Schölkopf])  
graphical models ([Jordan, 1998][1998_Jordan])

[LeCun, 1998][1998_LeCun], [Bengio, 2001][2001_Bengio]


3rd wave of NN

deep belief network trained using **greedy layer-wise pretraining** ([Hinton, 2006][2006_Hinton])  
[Bengio, 2007][2007_Bengio], [Ranzato, 2007][2007_Ranzato]  






### 01.02.02. Increasing Dataset Sizes

### 01.02.03. Increasing Model Sizes

### 01.02.04. Increasing Accuracy, Complexity and Real-World Impact




##
[01. Introduction]: https://www.deeplearningbook.org/contents/intro.html

<!-- toc -->
[0101]: #0101_who_should_read_this_book
[0102]: #0102_historical_trends_in_deep_learning
[010201]:  #010201_the_many_names_and_changing_fortunes_of_neural_networks
[010202]: #010202_increasing_dataset_sizes
[010203]: #010203_increasing_model_sizes
[010204]: #010204_increasing_accuracy_complexity_and_real-world_impact

<!-- ref -->
[slide]: http://www.deeplearningbook.org/slides/01_intro.pdf

[1943_Pitts_McCulloch]: #010201
[1958_Rosenblatt]: #010201
[1962_Rosenblatt]: #010201
[1960_Hoff_Widrow]: #010201
[1969_Papert_Minsky]: #010201
[2005_Field_Olshausen]: #010201
[2000_VonMekshner]: #010201
[1980_Fukushima]: #010201
[1998_KeCun]: #010201
[1975_Fukushima]: #010201
[2010_Hinton_Nair]: #010201
[2011_Glorot]: #010201
[2009_Jarrett]: #010201
[1986_Rumelhart]: #010201
[1995_McClelland]: #010201
[1985_Minton_Touretzky]: #010201
[1949_Hebb]: #010201
[1986_Hinton]: #010201
[1987_LeCun]: #010201
[1991_Hochreiter]: #010201
[1994_Bengio]: #010201
[1997_Schmidhuber_Hochreiter]: #010201
[1992_Boser]: #010201
[1995_Vapnik_Cortes]: #010201
[1999_Schölkopf]: #010201
[1998_Jordan]: #010201
[1998_LeCun]: #010201
[2001_Bengio]: #010201
[2006_Hinton]: #010201
[2007_Bengio]: #010201
[2007_Ranzato]: #010201

<!-- fig -->

<!-- term -->

<style type="text/css">
	img{width: 51%; float: right;}
</style>