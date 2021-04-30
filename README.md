# bigmart-sales-prediction-with-ibm-cloud-autoai

## This tutorial demonstrate how to create and deploy machine learning model with IBM’s AutoAI. Read medium blog post of this tutorial [BLOG HERE!](https://medium.com/@sha-rah646/how-to-create-and-deploy-machine-learning-model-with-watson-studio-autoai-ca1c772124c6)

<h4>Overview:</h4>
<p>In this tutorial, you will explore the following topics. </p> 
<ul>
  <li>Watson Studio Service</li>
  <li>Cloud Object Storage </li>
  <li>Machine Learning Instance </li>
  <li>Explore the data set </li>
  <li>IBM Cloud Notebook </li>
  <li>Training the machine learning model with data set in AutoAI experiment</li>
  <li>Deploy and Test model with sample data</li>
  <li>BigMartAutoAI Web Application</li>

</ul>
<h4>Activities:</h4>
<ul>
  <li>Create the Watson Studio.</li>
  <li>Adding the cloud object storage.</li>
  <li>Create Machine Learning Instance</li>
  <li>Training and Deploying the Auto AI Experiment.</li>
  <li>Predicting the output by providing an input to machine learning model.</li>
</ul>
<hr>

## Step-0: Explore Data Set, Notebook and Web App Demo
<ul>
<li>For this tutorial, we will use <code>BigMart Sales</code> data set from Kaggle. You can find dataset <strong><a href="https://www.kaggle.com/brijbhushannanda1979/bigmart-sales-data">here</a></strong>.</li>
<li>Data set <code>Exploration Analysis (EDA)</code> and <code>Notebook</code> of this tutorial you can find <strong>
<a href="https://tinyurl.com/pht9bc9z">here</a></strong>.</li>
<li>BigMartAutoAI web application demo <strong><a href="https://tinyurl.com/5t4hs4bc">here</a></strong>.</li>
</ul>

<br>

## Step-1: Create the Watson Studio Instance
<ul>
<li>Sign-up/Login to IBM Cloud: https://cloud.ibm.com/registration</li>
<li>After logging into the Cloud IBM Account, navigate to Catalog.</li>
<li>Click on the  <code>Watson Studio</code> </li>
</ul>
<img src="images/ibm_watson_1.png">
<ul>
	<li>You will be redirected to Watson studio page where you can create your Watson studio service
instance. There you click on <code>create</code> button.</li>
</ul>
<img src="images/ibm_watson_2.png">

<ul>
	<li>Now you will be redirected to the below page there click on <code>Get Started</code></li>
</ul>

<img src="images/ibm_watson_3.png">

<ul>
	<li> It will redirect to new page where you can create project, click on <code> Create a project </code>.</li>
</ul>

<img src="images/ibm_watson_4.png">

<ul>
	<li>Click on <code>Create an empty project</code></li>
</ul>

<img src="images/ibm_watson_5.png">

<hr>

## Step 2: Adding the Object Storage to project

<ul>
	<li>While creating the project you need to provide name and you need to select the object storage
service, on the right side under the storage service option you have an <code>ADD</code> option click on that.</li>
</ul>

<img src="images/ibm_watson_cloud_1.png">

<ul>
	<li>It will redirect to the new tab where we need to add the <code>Cloud Object storage</code> service. If you have
already created a cloud object storage service, you can select the existing instance. Or you need to
		<code>create</code> the new service instance.</li>
</ul>

<img src="images/ibm_watson_cloud_2.png">


<ul>
	<li>After Successful creation of object Storage Service, it will redirect to pervious page there you need to
select the object storage service which you have created in your previous step. If you did not get your
service name, simply click on the refresh button there.</li>

<li>After selecting the Cloud Object Storage service click on <code>create</code>. Then your project will be created.</li>

</ul>

<img src="images/ibm_watson_6.png">

<hr>

## Step-3: Creating an Auto AI Experiment

<ul>
	<li>After creating the project, you will get the below page.</li>

<li>On the top of screen you will have “add to project” option, Click on <code>Add to project</code></li>

</ul>

<img src="images/ibm_watson_7.png">


<ul>
	<li>Here you need to Select <code>AUTO AI experiment</code> as the asset type</li>
</ul>

<img src="images/ibm_watson_8.png">


<ul>
	<li>In this page we need to create Auto AI experiment and we need to select the Watson machine learning
service instance.</li>

<li>To create machine learning service instance open a new tab and navigate to project dashboard </li>

</ul>

<img src="images/ibm_watson_9.png">


<ul>
	<li>Click on the <code>Settings</code></li>

</ul>

<img src="images/ibm_watson_34.png">

<ul>
	<li>Scroll down to associated services</li>

<li>Click on the <code>Watson</code> from “Add service” drop down
</li>

</ul>

<img src="images/ibm_watson_35.png">


<ul>
	<li>Now you click on <code>Machine Learning</code> and then click on <code>create</code></li>

</ul>

<img src="images/ibm_watson_11.png">

<ul>
	<li>Once the Machine Learning Instance is created successfully it will redirect to previous page there you
reload page and select your machine learning instance which you have created and click on <code>associate service</code>.</li>

</ul>

<img src="images/ibm_watson_10.png">

<ul>
	<li>Now go to previously opened “New AutoAI experiment “ tab and reload page you will see machine
learning instance appeared you have created in above step.</li>

<li>Click on <code>Create</code>
</li>

</ul>

<img src="images/ibm_watson_18.png">

<hr>

## Step 4: Training and Deploying the Auto AI Experiment.

<ul>
	<li>After successfully creating a AutoAI Experiment, we need to upload the Data Set.</li>

<li>Just click on <code>Browse</code> option and select your dataset. You can also <code>select from project</code> if you already uploaded dataset to project</li>

</ul>

<img src="images/ibm_watson_19.png">

<ul>
<li>After selecting the file,Select the prediction column from the data set. You can also explore <code>Experiment Settings</code>, for now I will keep default settings and click on <code>Run Experiment</code></li>
</ul>

<img src="images/ibm_watson_20.png">

<ul>
	<li>After clicking on Run Experiment it will load the page with Progress map and it will start training your
model.</li>

<li>Wait till the progress map complete its operations with different algorithms to show the best suited
algorithm for Our Data set.</li>

</ul>

<img src="images/ibm_watson_222.png">
<ul>
<li>Now we can see ranking of different algorithms on this dataset.
</li
<li>We will select the Best algorithm and save
	the model by clicking the <code>save as</code> option. You can also save as Notebook and explore source code of your created model.</li>
<li>For now we will save it as model.</li>
</ul>
<img src="images/ibm_watson_22.png">

<ul>
<li>Wait till model is successfully saved. You will get the notification once it is saved. Now you click on <code>View in projects</code></li>
</ul>
<img src="images/ibm_watson_23.png">

<ul>
	<li>Now we will deploy our model. Select the <code>promote to deployment space</code> option.</li>
</ul>
<img src="images/ibm_watson_24.png">

<ul>
<li>It will redirect to the new tab where we need to add a deployment space. If you have already created a
deployment space , you can select the existing instance. Or you need to create the new service instance.</li>
</ul>
<img src="images/ibm_watson_25.png">

<ul>
<li>Now fill up deployment space name, storage service and machine learning service</li>
	<li>Click on <code>create</code></li>
</ul>
<img src="images/ibm_watson_26.png">
<ul>
<li>Wait till model is successfully promoted. You will get the notification once it is promoted. Now you
	click on <code>deployment space</code> in projects</li>
</ul>
<img src="images/ibm_watson_27.png">
<ul>
	<li>Click on <code>deployment icon</code> of our model
</li>
</ul>
<img src="images/ibm_watson_28.png">
<ul>
	<li>Now select <code>Online</code> and click on <code>Create</code>
</li>
</ul>
<img src="images/ibm_watson_29.png">
<ul>
<li>Now you can see project deployment dashboard, click on Deployments tab.
</li>
<li>Once you get the status as Deployed it means that your deployment is done successfully.
</li>
<li>Now you click on the deployment name.
</li>
</ul>
<img src="images/ibm_watson_31.png">
<ul>
<li>After Clicking on deployed project name, you will get Options like API reference, Code snippets, and Test. You can explore all of them.
</li>
	<li>We will test our deployed model so click on <code>Test</code>.
</li>
</ul>
<img src="images/ibm_watson_31.png">
<ul>
<li>In this Test tab, we need to give the input parameters to predict the output from our deployed model.
</li>
<li>After providing the input parameters click on the predict button to check the output of our machine learning model created and deployed using autoai.
</li>
</ul>
<img src="images/ibm_watson_33.png">


<br>

<br>



### Useful Resources

<ul>
<li>
Watson Studio AutoAI : <a href="https://www.ibm.com/cloud/watson-studio/autoai?cm_sp=freelancer-_-AutoAI-_-cta" target="_blank">https://www.ibm.com/cloud/watson-studio/autoai</a>
</li>
<li>
Step by step tutorials : <a href="https://www.ibm.com/cloud/garage/dte/tutorial/ibm-watson-studio-autoai-modeling-rest-us?cm_sp=freelancer-_-AutoAI-_-cta" target="_blank"> https://www.ibm.com/cloud/garage/dte/tutorial/ibm-watson-studio-autoai-modeling-rest-us</a>	
</li>	
<li>Video tutorials : <a href="https://www.youtube.com/watch?v=knxbJgPmD5E" target="_blank">https://www.youtube.com/watch?v=knxbJgPmD5E</a>
</li>
<li>Documentations : <a href="https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/autoai-overview.html?cm_sp=freelancer-_-AutoAI-_-cta" target="_blank">https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/autoai-overview.html</a>
</li>
</ul>
