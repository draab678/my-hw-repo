### ***Final Project Feedback***

***Nico Van de Bovenkamp***

***

**Overall**  
Great work on this first crack at a model. It is clear that your business/finance acumen is helping you a ton when you're building out this model. I am sure this felt dramatically more comfortable than when we take a fairly obscure dataset and try to build out models (very few people actually have any knowledge of biking culture, NYC, and urban planning to have insights that are this effective).

Additionally, great job using some functions for your model building and pipelining! That is a really good habit as you program more and more. You will find that you save tons of time and can debug much faster if you modularize your code like so. I do have a few recommendations though, which you can see below.

**Recommendations**  

***Building functional code***  
It's very curious that your model would have exactly the same outputs when you shifted the time-step a day. It's likely that there is something weird going on in Jupyter notebooks and your "test" and "train" objects are getting stored (darn notebooks). What I recommend is you make your code a little more modular by making that `run_model()` function take in a train, test, and array of choices, eg: `run_model(train, test, choices)` this way your variables maintain the scope you are looking for. Plus, you get a little more flexibility! In addition, you could pass in some other parameters, like a parameter dictionary for your logistic regression!

***Hyper-parameters***  
While other model architectures (eg. SVMs vs. logistic regression vs. Decision Trees vs. Random Forrest) will yield very different results, ensure that you are taking advantage of other hyper-paramters. Make sure you experiment with different forms of regularization (L1 may be nice for sparse data like this), kernels if you are using SVMs, num_trees, split sizes, etc. These are very important to your over all model success, especially in problems this challenging!

***Extracting different features***  
In addition to playing with the ngrams (very good move, by the way!), I recommend that you experiment with some other feature extractors, like the TfIdfVectorizer that we used in class. It's not guaranteed to improve everything, but it will encode different information into your model!

Additionally, make sure you are taking care of cleaning and managing your text data. When it comes to text, having messy inputs will lead to messy models. You should make sure that you are simplifying your text so that you are pulling out the best information you can. This means you want to standardize your text (via lower-casing typically), strip punctuation, try and avoid useless spacing (white spacing), and pulling out what are called "stop-words" (words that likely don't encode much, if any, information but add tons of complexity to your model like: the, about, and, or, etc.).

Taking these steps will definitely give you some lift even before you start playing with other models! s
