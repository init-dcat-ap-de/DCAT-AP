# Usage guide on Datasets, Distributions and Data Services

The introduction of Data Services as first class citizens in DCAT 2.0 raised questions about the usage of Data Services and Distributions.
This section provides a guideline for publishers what to consider as a Distribution and what as a Data Service.

A first distinction between distributions and data services is their dependency on a dataset for their existance. A distribution cannot exist without its dataset. It is a specific representation of a dataset (cfr definition W3C https://w3c.github.io/dxwg/dcat/#Class:Distribution) Whereas a data service is an entity in its own right. It provides access to datasets or it provides data processing functions. The independence also holds between the distributions of a dataset, and the data service which provides access to that dataset. The distributions are not only the result of the data service operations. However, they may.  

Many of the properties of distributions are file oriented (downloadURL, format, byte size, checksum, modification date, ...). The relevance of this information is reduced for data services, related information is present in a very different form and thus under different terminology. For instance, data services do and can provide format transformations, language transformations and schema transformations on request. Also the handling of trust is different. While tampering of downloadable content is detected by e.g. checksums, data services create often a trusted channel using security measures such as authentication and encryption. This reduces the need for additional trust checks on the data. 

The difference between downloading a file or accessing the data through a service have resulted in the following guidelines:
  - datasets are the conceptual entity denoting a collection of data
  - distributions are specific representations of a dataset, described with the intend to facilitate the delivery of the data as file to a reuser. The access URL (preferably download URL) will provide a simple way to obtain (download) the content of the dataset in the representation specified by the distribution. The obtained (downloaded) content is fully determined by the publisher of the distribution. Only after obtaining the data the (re)user can change the data according to its needs. 
  - Anything that has not the intend to provide a downloadable representation of a dataset is a data service. Data services offer smarter, more interactive ways to the data.   

The guidelines will be able to capture many access patterns, corresponding to most users' expectations. However there might be cases that are more vague. In that case the DCAT(-AP) community can be questioned for a recommended approach.