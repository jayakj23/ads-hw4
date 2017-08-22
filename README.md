# Social Networks with AWS Rekognition and Neo4j
This is a Jupyter notebook that highlights the use of AWS Rekognition's facial identification functionality.  It will identify celebrity faces (http://docs.aws.amazon.com/rekognition/latest/dg/celebrity-recognition.html) and use the Movie Graph Database (https://neo4j.com/developer/movie-database/#_download) hosted in a Neo4J instance to render a graphical representation of the relationship between two celebrities (ala Six Degrees of Kevin Bacon).

## Setup
Cloudformation templates are located under <project>/cft.  Run the following:
```
aws cloudformation create-stack –-stack-name rekognitionblog \
  --template-body file://rek-neo4j-blogpost-git.template \
  --parameters ParameterKey=KeyName,ParameterValue=<YOURKEYHERE> \
  --capabilities CAPABILITY_NAMED_IAM
```



