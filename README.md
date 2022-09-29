<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {font-family: Arial;}

/* Style the tab */
.tab {
  overflow: hidden;
  border: 1px solid #ccc;
  background-color: #f1f1f1;
}

/* Style the buttons inside the tab */
.tab button {
  background-color: inherit;
  float: left;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 14px 16px;
  transition: 0.3s;
  font-size: 17px;
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: #ddd;
}

/* Create an active/current tablink class */
.tab button.active {
  background-color: #ccc;
}

/* Style the tab content */
.tabcontent {
  display: none;
  padding: 6px 12px;
  border: 1px solid #ccc;
  border-top: none;
}
</style>
</head>
<body>

<h2>Person Detection for Social Distancing using Computer Vision</h2>

<div class="tab">
  <button class="tablinks" onclick="openCity(event, 'Home')">Home</button>
  <button class="tablinks" onclick="openCity(event, 'Architecture')">Architecture</button>
  <button class="tablinks" onclick="openCity(event, 'Methodology')">Methodology</button>
  <button class="tablinks" onclick="openCity(event, 'Conclusion and Future Scope')">Conclusion and Future Scope</button>



</div>



<div id="Home" class="tabcontent">
  <h3>Introduction</h3>
  <p>
  Coronavirus is a large family virus that harms humans and animals. Covid-19 is known as a family member of coronavirus, first spread to Wuhan, China in December 2019. The outbreak then rapidly affected many countries in the world and had been declared as a pandemic by the World Health Organization (WHO). Based on the information from WHO, the coronavirus is spreading from a person to a person via small droplets from the nose and mouth. In other words, social distancing is the best practice where people can minimize physical contact with possible coronavirus carriers, by keeping the distance at least one meter away from each other.
The project “Person Detection for Social Distancing” is proposed to support the actions on Covid-19 spread mitigation. It provides a solution for detecting people gathering in public places such as banks, shopping malls, clinics etc. The concept of person detection algorithm is used to accurately detect a person’s presence in areas of interest and is then followed by measuring the distance between the detected persons.

  </p>
  <h3>Existing System</h3>
  <p>Since the novel coronavirus pandemic began, many countries have been taking the help of technology based solutions in different capacities to contain the outbreak. Many developed countries, including India and South Korea, for instance, utilizing GPS to track the movements of the suspected or infected persons to monitor any possibility of their exposure among healthy people. In India, the government is using Arogya Setu app, which works with the help of GPS and Bluetooth to locate the presence of Covid-19 patients in vicinity area. It also helps others to keep safe distance from the infected person.
On the other hand, some law enforcement departments have been using drones and other surveillance cameras to detect mass gatherings of people, and taking regulatory actions to disperse the crowd. Human detection using visual surveillance system is an established area of research which is relying upon manual methods of identifying unusual activities. However, it has limited capabilities.
 
   </p><h3>Problems in existing system</h3><p>
•	Time Consuming
•	Brings a unique set of threats to the public and is challenging to the workforce
</p> 
 <h3>Proposed System</h3>
  <p>
  In the proposed system, a deep learning based framework is proposed that utilizes object detection and tracking models to aid in the social distancing remedy for dealing with the escalation of Covid-19 cases. In order to maintain the balance of speed and accuracy, SSD (Single Shot Detector) algorithm is utilized as object detection and tracking approaches while surrounding each detected object with the bounding boxes.
Later, these bounding boxes are utilized to compute the pair wise L2 norm with computationally efficient vectorized representation for identifying the clusters of people not obeying the order of social distancing.
</p><h3>	Benefits of Proposed System</h3>
<p>
•	Reduces the transmission of viruses by following a non-pharmaceutical way
•	Time saving
•	User friendly</p>
 

  
 

</div>

<div id="Architecture" class="tabcontent">
  <h3>Software Architecture</h3>
  <p>Software architecture exposes the structure of a system while hiding the implementation details. Architecture also focuses on how the elements and components within a system interact with one other. Software design delves deeper into the implementation details of the system</p>

<img src="https://drive.google.com/file/d/1zDpu2gDBqPr6uD4qdJfiGcn3gBu68BHL/view?usp=sharing" alt=”Software Architecture” width="400" height="200">

</img>
<h3>Technical Architecture</h3>
<p>
The technical architecture of the platform is modelled following the well-known and field tested three-tier architecture. This model proposes logical and physical separation of concerns (data access, business logic and presentation) in layers, with an
 
emphasis on maintainability and decoupling of components. The separation in layers (logical separation) and/or tiers (physical separation) allows for separate evolution, or even replacement, of the different components of the system, with changes in one layer not compromising other layers.
Front end provides the visibility of application to the user and whereas middle ware provides the linkage between back end and front end and back end stores the data for the application.

</p>
<img src="https://drive.google.com/file/d/1W8kmQKxDRQWTZL7pTquWX_S3E9095hJ0/view?usp=sharing" alt=”Technical Architecture” width="400" height="200">

</img>

</div>

<div id="Methodology" class="tabcontent">
  <h3>Trained Model</h3>
  <p>In order to have a robust detector, a set of rich training datasets are required. This should include people with a variety in gender and age with millions of accurate annotation and labelling. We selected SSD_MobileNet model trained with two large datasets of MS COCO(Common Objects in Context) and Pascal VOC dataset.
</p>

<h3>People Detection
</h3>
<p>
The SSD_MobileNet model is able to detect humans (people) with various types of challenges such as variations in clothes, postures, at far and close distances, with or without occlusion, and under different lighting conditions.

</p>
<h3>Inter-distance Estimation
</h3>
<p>
After detection, the bounding box information, mainly centroid information is used to compute each bounding box centroid distance. Euclidean distance can be used to calculate the distance between each detected bounding box of peoples.
Following computing centroid distance, a predefined threshold is used to check either the distance among any two bounding box centroids is less than the configured number of pixels or not. 
If two people are close to each other and the distance value violates the minimum social distance threshold then the bounding box information is stored in a violation set and the color of the bounding box is updated or changed to red.
</p>
<img src="https://drive.google.com/file/d/1o_HF6DRYvq3wayW6fTx6eg25d5EGnHEi/view?usp=sharing" alt=”Technical Model” width="400" height="200">

</img>

</div>

<div id="Conclusion and Future Scope" class="tabcontent">
  <h3>Conclusion</h3>
  <p>
  Social distancing is one of the important precautions in reducing physical contact that may lead to the spread of coronavirus. Consequences of non-compliance with these guidelines will be causing the higher rates of virus transmission. The proposed project has an efficient real-time deep learning based framework to automate the process of monitoring the social distancing via object detection, where each individual is identified in the real-time with the help of bounding boxes.
Thus, this project can reduce the on ground efforts of the police and they can entirely focus on supervising conditions exclusively on those areas where conditions are unfavorable and thus, they can utilize time wisely and save energy for equitable situations.
</p>
  
  <h3>Future Scope</h3>
<p>
A single viewpoint obtained from a single camera cannot reflect the result more effectively. Therefore, the proposed application may be set for different views through many cameras in the future to get more accurate results.
 

</p>
</div>




<script>
function openCity(evt, cityName) {
  var i, tabcontent, tablinks;
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }
  document.getElementById(cityName).style.display = "block";
  evt.currentTarget.className += " active";
}
</script>
   
</body>
</html> 
