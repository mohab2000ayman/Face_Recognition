# Pattern Recognition Course Assignment 1: Face Recognition

### Authors:Mohab Ayman & Anas Emad & Mazen Ahmed at March 2023

## Introduction

Face recognition has become a major field of interest these days. Face recognition algorithms are used in a wide range of applications such as security control,crime investigation, and entrance control in buildings, access control at automatic teller machines, passport verification, identifying the faces in a given databases. Formally, Face recognition is the bio-metric identification by scanning a person’s face and matching it against a library of known faces.
In this assignment, we implement two different image recognition approaches.
The first is Eigenfaces which is one of the most widely used representations, which are based on principal component analysis and use a nearest neighbour classifier. The second is Fisherfaces which use linear/Fisher discriminant analysis (FLD/LDA) for best discriminating the face images of same class and also use a nearest neighbour classifier.

## Approach one: Classification using Eigenfaces and Principal component analysis

PCA is also known as Karhunen Loeve projection.Principal component analy-
sis (PCA) is a statistical procedure that uses an orthogonal transformation to
convert a set of observations of possibly correlated variables (entities each of
which takes on various numerical values) into a set of values of linearly uncor-
related variables called principal components and refrred to as Eigenfaces. In
PCA, the main idea to re-express the available dataset to extract the relevant
information by reducing the redundancy and minimize the noise. A nearest
neighbour classifier works afterwards by comparing compare a face’s position in
Eigenfaces subspace with the position of known individuals and the distances
between them.



## Approach two: classification using Linear Discriminant Analysis

Linear discriminant analysis (LDA), also called normal discriminant analysis
(NDA), or discriminant function analysis is a generalization of Fisher’s linear
discriminant, a method used in statistics, pattern recognition and machine learn-
ing to find a linear combination of features that characterizes or separates two
or more classes of objects or events.
Ronald A. Fisher formulated the Linear Discriminant in 1936 in [3], and it also
has some practical uses as classifier. The original Linear discriminant was de-
scribed for a 2-class problem, and it was then later generalized as “multi-class
Linear Discriminant Analysis” in [4].
The goal of LDA is to project a feature space (a dataset n-dimensional samples)
onto a smaller subspace k (where k is smaller than or equal to n-1) while main-
taining the class-discriminatory information. In other words, it seeks to reduce
dimensionality while class separation in mind.


### PCA vs LDA

LDA is also closely related to principal component analysis (PCA) and in that
they both look for linear combinations of variables which best explain the
data.LDA explicitly attempts to model the difference between the classes of
data. PCA on the other hand does not take into account any difference in class,
and factor analysis builds the feature combinations based on differences rather
than similarities.

Both Linear Discriminant Analysis (LDA) and Principal Component Anal-
ysis (PCA) are linear transformation techniques that are commonly used for di-
mensionality reduction. PCA can be described as an “unsupervised” algorithm,
since it “ignores” class labels and its goal is to find the directions (the so-called
principal components) that maximize the variance in a dataset. In contrast to
PCA, LDA is “supervised” and computes the directions (“linear discriminant”)
that will represent the axes that that maximize the separation between multiple
classes. Although it might sound intuitive that LDA is superior to PCA for a
multi-class classification task where the class labels are known, this might not
always the case. For example, comparisons between classification accuracies for
image recognition after using PCA or LDA show that PCA tends to outperform
LDA if the number of samples per class is relatively small as shown in [5]. In
practice, it is also common to use both LDA and PCA in combination: E.g.,
PCA for dimensionality reduction followed by an LDA, this approach is called
the Fisher Faces and was proposed in [6]. As we mention later on, one of our


future improvement tasks is to implement this approach and compare it with
our work here. Also in case of uniformly distributed data, LDA almost always
performs better than PCA. However if the data is highly skewed (irregularly
distributed) then it is advised to use PCA since LDA can be biased towards the
majority class.



## References

[1]Data Mining and Analysis: Fundamental Concepts and Algorithms MO-
HAMMED J. ZAKI Rensselaer Polytechnic Institute, Troy, New York WAG-
NER MEIRA JR. Universidade Federal de Minas Gerais, Brazil

[2]ATT Face database, or formally ORL Faces

[3]”The Use of Multiple Measurements in Taxonomic Problems” by Ronald A.
Fisher in 1936

[4]”Multiple Discriminant Analysis” by C. R. Rao in 1948

[5]PCA vs. LDA, A.M. Martinez et al., 2001

[6]”Eigenfaces vs. Fisherfaces: Recognition Using Class Specific Linear Pro-
jection” by Peter N. Belhumeur, Joao P. Hespanha, and David J. Kriegman

[7]FACE RECOGNITION USING PCA, LDA AND VARIOUS DISTANCE
CLASSIFIERS
