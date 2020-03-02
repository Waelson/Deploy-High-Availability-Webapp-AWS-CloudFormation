# deploy-high-availability-webapp-cloudformation
Deploying high availability web application on Apache Server using AWS Cloudformation.
<br/>
<h4>Importante notes:</h4>
<ul>
  <li>You will need to create a Key Pair through web console, to edit servers.yml file and to update value of the KeyName attribute in the resource AWS::AutoScaling::LaunchConfiguration</li>
</ul>  
    
Theses templates allow you to create infrastructure and deploy a web application based on Apache Server using AWS Cloudformation.
<br/>
<h4>How to use:</h4>
<ul>
  <li>First, create infrastructure network: <code>aws cloudformation create-stack --stack-name network --template-body file:///&#60your-path&#62/network.yml --parameters file:///&#60your-path&#62network-params.json</code></li>
    <li>Last, create servers and other resources: <code>aws cloudformation create-stack --stack-name servers --template-body file:///&#60your-path&#62/servers.yml --capabilities CAPABILITY_IAM --parameters file:///&#60your-path&#62/servers-params.json</code></li>  
 </ul>
<h4>Solution diagram:</h4>
<img src="https://github.com/Waelson/deploy-high-availability-webapp-cloudformation/blob/master/diagram.png">
