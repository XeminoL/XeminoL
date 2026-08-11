<div align="center">

<img src="https://readme-typing-svg.demolab.com/?font=JetBrains+Mono&weight=700&size=30&pause=1400&color=7EE787&center=true&vCenter=true&width=560&height=60&lines=Dang+Thai+Khang;Computer+Engineering+%40+HCMUT" alt="Dang Thai Khang" />

</div>

<br/>

```console
~/khang $ cat stack.txt

  languages        Python, JavaScript, HTML, CSS
  cloud            AWS (Lambda, S3, DynamoDB, API Gateway, Cognito)
  ai               Bedrock, Rekognition, Textract, Word2Vec, KMeans
  tools            Flask, Hugo, NumPy, scikit-learn, OR-Tools

~/khang $ ls projects/
  insightshare/    serverless document assistant on AWS
  slotwise/        picks warehouse storage locations from order history
```

<br/>

### insightshare

Capstone for the First Cloud AI Journey internship at AWS Vietnam. Upload an image or
PDF and it becomes searchable: Rekognition labels images, Textract pulls text out of
documents, and Bedrock answers questions about what it read. Files sit in a private S3
bucket and move through short-lived presigned URLs.

One Python Lambda behind API Gateway, Cognito for sign-in, DynamoDB for metadata,
ap-southeast-1. This repo holds the workshop that walks through building it.

[repo](https://github.com/XeminoL/InsightShare) &middot; [workshop](https://xeminol.github.io/InsightShare/) &middot; [demo](https://insightshare.dangthaikhang34.workers.dev/)

### slotwise

A warehouse keeps reserve stock upstairs in zone R and picking stock downstairs in
zone A. When A runs low, a forklift brings a pallet down. Slotwise reads the order log
and decides which R aisle an incoming item belongs in, so those trips stay short.

Score is `0.6 x near_refill_target + 0.4 x near_companions`. The first half uses the
median of the item's zone A cluster, since travel is measured in L1 and the median is
what minimizes it. The second half comes from Word2Vec over the order log, treating
each order as a sentence, to keep items that ship together stored together.

Flask, gensim, scikit-learn, UMAP. The heuristic is checked against OR-Tools CP-SAT.

[repo](https://github.com/XeminoL/slotwise)

<br/>

<div align="center">
  <img src="https://github.com/XeminoL/XeminoL/blob/output/github-snake-dark.svg" alt="contribution snake" width="88%" />
</div>
