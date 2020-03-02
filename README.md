# deploy-high-availability-webapp-cloudformation
Deploying high availability web application on Apache Server using AWS Cloudformation.
<br/>
Theses templates allow you to create infrastructure and deploy a web application based on Apache Server using AWS Cloudformation.
<br/>
<h4>How to use:</h4>
<ul>
  <li>First, create infrastructure network: <code>aws cloudformation create-stack --stack-name network --template-body file:///<your-path>/network.yml --parameters file:///<your-path>network-params.json</code></li>
    <li>Last, create servers and other resources: <code>aws cloudformation create-stack --stack-name servers --template-body file:///<your-path>/servers.yml --capabilities CAPABILITY_IAM --parameters file:///<your-path>/servers-params.json</code></li>  
 </ul>
<h4>Solution diagram:</h4>
<img src="https://github.com/Waelson/deploy-high-availability-webapp-cloudformation/blob/master/diagram.png">
