# deploy-high-availability-webapp-cloudformation
Deploying high availability web application on Apache Server using AWS Cloudformation.
<br/>
<br/>
Theses templates allow you to create infrastructure and deploy a web application based on Apache Server using AWS Cloudformation.
<br/>
<h4>Important note:</h4>
<ul>
  <li>You can specify S3 bucket and file name where the stack can to get the code your application in the file <code>servers.yml</code> to deploy it.</li>
</ul>  
<h4>How to use:</h4>
<ul>
  <li>First, create infrastructure network: <code>aws cloudformation create-stack --stack-name network --template-body file:///&#60your-path&#62/network.yml --parameters file:///&#60your-path&#62network-params.json</code></li>
    <li>Last, create servers and other resources: <code>aws cloudformation create-stack --stack-name servers --template-body file:///&#60your-path&#62/servers.yml --capabilities CAPABILITY_IAM --parameters file:///&#60your-path&#62/servers-params.json</code></li>  
 </ul>
<h4>Solution diagram:</h4>
<img src="https://github.com/Waelson/deploy-high-availability-webapp-cloudformation/blob/master/diagram.png">
