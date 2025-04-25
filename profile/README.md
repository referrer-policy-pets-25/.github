# Referrer Policy: Implementation and Circumvention (PETS'25)

This repository contains the crawler code and jupyter notebook for our paper [Referrer Policy: Implementation and Circumvention]()

## Abstract

The Referrer Policy (RP) standard makes it possible for websites to control how much information will be shared in the Referer _[sic]_ header. In this study, we investigate the implementation and circumvention of the Referrer Policy standard across 27,750 distinct websites and over 100K pages from three vantage points: the United States, Singapore, and the Netherlands.

Our findings reveal that 48.38% of websites implement document-wide referrer policies, and 13.39% apply element-specific referrer policies. The majority of the sites (43.81%) use the Referrer-Policy HTTP response header to set a document-wide policy, while 11.09% use HTML meta tags. Even on websites with restrictive referrer policies, scripts can access the full page URL and exfiltrate it --- which we label as a referrer policy circumvention.

We identified RP circumventions on 77.20% of websites often carried out by third-party advertising and analytics scripts, including Google Analytics, Facebook, and TikTok Pixel. While the ability to manage referrer information and the adoption of more privacy-focused default policies represent positive gains for user privacy, the widespread circumvention of these measures by third-party scripts remains to be a problem. We recommend implementing technical measures to restrict script access in order to address this privacy and security issue

## Contribution

In summary, we make the following contributions
- We measure the implementation of RP on more than 27K websites using vantage points from three continents **North America, Asia, and Europe**.
- We study how websites implement RP, by analyzing HTTP headers, _meta_ element attributes, element-specific policies and relational attributes _rel_.
- We develop a method to detect and measure _RP circumventions_, building on a leak detection method from prior [work](https://github.com/leaky-forms/leaky-forms).
