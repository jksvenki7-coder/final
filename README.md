# final<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>JKS Group Unified App</title>
<style>
  body {
    background: #20242b;
    color: #fff;
    font-family: 'Segoe UI', Arial, sans-serif;
    margin: 0; padding: 0;
  }
  header, nav {
    display: flex; justify-content: center; gap: 20px;
    background: #141b29; padding: 18px 0;
    box-shadow: 0 2px 6px rgba(0,0,0,0.7);
    position: sticky; top: 0; z-index: 1000;
  }
  header {
    font-weight: 700; font-size: 1.6em; color: #00e1ff;
    text-shadow: 0 0 14px #0fccfcc5;
  }
  nav button {
    background: none;
    border: 2.5px solid #0fccfc;
    border-radius: 9px;
    color: #0fccfc;
    font-weight: 700;
    font-size: 1em;
    cursor: pointer;
    padding: 14px 24px;
    transition: 0.3s ease;
    user-select: none;
  }
  nav button:hover {
    background: #0fccfc;
    color: #181f30;
  }
  main {
    max-width: 1120px;
    margin: 36px auto 70px auto;
    padding: 0 16px;
  }
  .main-title {
    font-size: 2.3em;
    color: #00e1ff;
    font-weight: 700;
    margin-bottom: 40px;
    letter-spacing: 2px;
    text-align: center;
    text-shadow: 0 0 14px #0fccfcc5;
  }
  .dashboard {
    display: flex; flex-wrap: wrap;
    gap: 32px; justify-content: center;
  }
  .folder-card {
    background: #23273b;
    border: 3px solid #ffe27f;
    border-radius: 12px;
    padding: 44px 60px;
    font-weight: 700;
    font-size: 1.25em;
    color: #ffe27f;
    cursor: pointer;
    box-shadow: 0 0 16px 4px #fff68d90, 0 5px 26px #10172285;
    text-align: center;
    transition: 0.4s ease all;
    min-width: 240px;
    user-select: none;
  }
  .folder-card:hover {
    background-color: #ffe27f;
    color: #171e29;
    border-color: #0fccfc;
    box-shadow: 0 0 26px 7px #0fccfcc3, 0 7px 32px #23536f85;
    transform: scale(1.07);
  }
  .section-title {
    text-align: center;
    font-size: 1.7em;
    font-weight: 700;
    letter-spacing: 1.4px;
    margin: 24px auto 26px auto;
    color: #ffe27f;
    text-shadow: 0 0 16px #ffe27fb1;
  }
  .service-list, .category-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 28px;
    margin-bottom: 30px;
  }
  .service-card, .category-card, .event-card {
    background: #23273a;
    border: 2.5px solid #ffe27f;
    border-radius: 12px;
    min-width: 190px;
    max-width: 220px;
    padding: 24px;
    color: #ffe27f;
    font-weight: 700;
    font-size: 1.1em;
    cursor: pointer;
    text-align: center;
    box-shadow: 0 0 18px 3px #ffed8798, 0 5px 14px #1116227f;
    transition: background-color 0.3s ease, color 0.3s ease, transform 0.2s ease;
  }
  .service-card:hover, .category-card:hover, .event-card:hover {
    background-color: #ffe27f;
    color: #242d3a;
    border-color: #0fccfc;
    box-shadow: 0 0 20px 6px #0fccfcbb, 0 5px 28px #26405a8a;
    transform: scale(1.07);
  }
  .back-btn {
    display: block;
    margin: 32px auto 0 auto;
    background: #ffe27f;
    color: #252a39;
    font-weight: 800;
    border: 2.8px solid #ffe27f;
    border-radius: 15px;
    padding: 17px 60px;
    font-size: 1.2em;
    box-shadow: 2px 2px 22px #ffe27fca;
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease;
    user-select: none;
    width: max-content;
  }
  .back-btn:hover {
    background-color: #00e1ff;
    border-color: #00e1ff;
    color: #f5fbff;
    box-shadow: 0 0 30px 8px #00e1ffcc;
  }
  form.contact-form {
    max-width: 480px;
    margin: 40px auto 70px auto;
    padding: 28px 32px;
    background: #17243e;
    border-radius: 14px;
    border: 2px solid #0fccfccc;
    color: #90c8ff;
    font-size: 1.1em;
  }
  form.contact-form label {
    font-weight: 700;
    margin-bottom: 10px;
    display: block;
  }
  form.contact-form input, form.contact-form textarea, form.contact-form select {
    background: #11253b;
    border: 1.5px solid #0fccfab8;
    padding: 14px 18px;
    border-radius: 8px;
    color: #bcd9ff;
    font-size: 16px;
    margin-bottom: 24px;
    box-sizing: border-box;
    width: 100%;
    resize: vertical;
  }
  form.contact-form input:focus, form.contact-form textarea:focus, form.contact-form select:focus {
    outline: none;
    border-color: #00b6f1;
    background: #1b355c;
  }
  form.contact-form button {
    width: 100%;
    color: #193140;
    background: #00e1ff;
    font-weight: 900;
    font-size: 1.26em;
    border: none;
    border-radius: 12px;
    padding: 16px 0;
    cursor: pointer;
    transition: background-color 0.28s ease;
  }
  form.contact-form button:hover {
    background-color: #4ee7ff;
  }
  nav button.camera-map-btn {
    background: #3e7199;
    border-radius: 12px;
    padding: 14px 22px;
  }
  nav button.camera-map-btn:hover {
    background: #0ed6ff;
    color: #001220;
  }
  #camera video {
    width: 100%;
    max-width: 440px;
    border-radius: 15px;
    border: 2px solid #0fccfc;
    margin-top: 20px;
  }
  #maps {
    width: 100%;
    max-width: 600px;
    height: 460px;
    border-radius: 15px;
    margin: 20px auto 40px auto;
    border: 3px solid #0fccfccc;
    box-shadow: 0 0 40px 15px #0fccfc40;
  }

  @media (max-width: 900px) {
    .folders-wrap, .service-list, .category-list, .events-categories {
      flex-direction: column;
      gap: 20px;
      align-items: center;
    }
    .folder-card, .service-card, .category-card, .event-card {
      width: 90%;
      padding: 24px 16px;
      font-size: 1.07em;
    }
  }
</style>
</head>
<body>
<header><div class="main-title">JKS Group of Business</div></header>
<nav>
  <button onclick="showPage('dashboard')">Dashboard</button>
  <button onclick="showPage('profile')">Profile</button>
  <button onclick="showPage('wallet')">Wallet</button>
  <button onclick="showPage('orders')">Orders</button>
  <button class="camera-map-btn" onclick="showPage('camera')">Camera</button>
  <button class="camera-map-btn" onclick="showPage('maps')">Google Maps</button>
</nav>
<main>
  <section id="dashboard" class="dashboard">
    <div class="folders-wrap">
      <div class="folder-card" onclick="openModule('ecommerce')">My E-commerce</div>
      <div class="folder-card" onclick="openModule('events')">Events & Catering</div>
      <div class="folder-card" onclick="openModule('courier')">Courier & Ride Booking</div>
      <div class="folder-card" onclick="openModule('job')">Job Consultancy & Services</div>
      <div class="folder-card" onclick="openModule('tours')">Tours & Travels</div>
      <div class="folder-card" onclick="openModule('realestate')">Real Estate & Construction</div>
      <div class="folder-card" onclick="openModule('investment')">Investment & Business</div>
      <div class="folder-card" onclick="openModule('loans')">Loans & Insurance</div>
      <div class="folder-card" onclick="openModule('home')">Home Services</div>
    </div>
  </section>

  <section id="profile" style="display:none; text-align:center;">
    <h2 class="section-title">Profile</h2>
    <div class="contact-form" style="max-width:500px;margin:auto;">
      <label>Full Name:</label>
      <input type="text" id="profileName" placeholder="Enter your full name" />
      <label>Email:</label>
      <input type="email" id="profileEmail" placeholder="example@gmail.com" />
      <label>Phone:</label>
      <input type="tel" id="profilePhone" placeholder="Mobile number" />
      <label>Address:</label>
      <textarea id="profileAddress" rows="3" placeholder="Your address"></textarea>
      <button onclick="updateProfile()">Update Profile</button>
    </div>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>

  <section id="wallet" style="display:none; text-align:center;">
    <h2 class="section-title">Wallet</h2>
    <p>Your current wallet balance: <strong>₹10,000</strong></p>
    <p>Recent transactions will be listed here.</p>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>

  <section id="orders" style="display:none; max-width:600px; margin: 0 auto;">
    <h2 class="section-title">Orders</h2>
    <div id="ordersList">
      <p>No orders placed yet.</p>
    </div>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>

  <section id="serviceView" style="display:none; flex-direction: column; align-items: center;">
    <div class="section-title" id="serviceTitle"></div>
    <div class="service-list" id="serviceList"></div>
    <form class="contact-form" id="contactForm" style="display:none;">
      <h3 id="contactTitle"></h3>
      <label>Name:</label><input type="text" id="userName" required/>
      <label>Mobile Number:</label><input type="tel" id="userPhone" maxlength="10" pattern="[6-9][0-9]{9}" required/>
      <label>Message:</label><textarea id="userMessage" rows="4" required></textarea>
      <button type="button" onclick="submitContactForm()">Submit via WhatsApp</button>
      <button type="button" class="back-btn" onclick="backToServiceList()">Back to Services</button>
    </form>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>

  <section id="eventsView" style="display:none; flex-direction: column; align-items: center;">
    <div class="section-title" id="eventsCategoryTitle"></div>
    <div class="events-categories" id="eventsCategories"></div>
    <div class="service-list" id="eventsServiceList"></div>
    <form id="eventContactForm" class="contact-form" style="display:none;">
      <h3 id="eventsContactTitle"></h3>
      <label>Name:</label><input id="eventsUserName" type="text" required />
      <label>Mobile Number:</label><input id="eventsUserPhone" type="tel" pattern="[6-9][0-9]{9}" maxlength="10" required />
      <label>Budget:</label>
      <select id="eventsBudget">
        <option value="" disabled selected>Select Budget (if applicable)</option>
        <option value="10k to 50k">10k to 50k</option>
        <option value="50k to 1L">50k to 1L</option>
        <option value="1L to 5L">1L to 5L</option>
        <option value="5L to 10L">5L to 10L</option>
        <option value="Above 10L">Above 10L</option>
      </select>
      <label>Capacity:</label>
      <select id="eventsCapacity">
        <option value="" disabled selected>Select Capacity (if applicable)</option>
        <option value="5-30 people">5-30 people</option>
        <option value="30-60 people">30-60 people</option>
        <option value="60-90 people">60-90 people</option>
        <option value="90-130 people">90-130 people</option>
        <option value="Above 130 people">Above 130 people</option>
      </select>
      <label>Message:</label><textarea id="eventsUserMessage" rows="4" required></textarea>
      <button type="button" onclick="submitEventsForm()">Submit via WhatsApp</button>
      <button type="button" class="back-btn" onclick="backToEventsCategory()">Back to Category</button>
    </form>
    <button type="button" class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>

  <section id="ecomView" style="display:none;">
    <div class="section-title">My E-commerce</div>
    <nav>
      <button onclick="openEcomCategory('Groceries')">Groceries</button>
      <button onclick="openEcomCategory('Food')">Food</button>
      <button onclick="openEcomCategory('Pharmacy')">Pharmacy</button>
      <button onclick="showPage('camera')">Camera</button>
      <button onclick="showPage('maps')">Google Maps</button>
    </nav>
    <div id="ecomCategoryContent"></div>
    <div id="ecomFormSlot"></div>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>

  <section id="camera" style="display:none; text-align:center; padding: 10px;">
    <h2 class="section-title">Camera</h2>
    <video id="video" autoplay muted playsinline style="max-width: 90%; border-radius: 12px; border: 2px solid #0fccfc;"></video>
    <div style="margin-top: 15px;">
      <button onclick="switchCamera()">Switch Camera</button>
      <button onclick="capturePhoto()">Capture Photo</button>
      <button class="back-btn" onclick="showPage('ecomView')">Back to E-commerce</button>
    </div>
    <canvas id="canvas" style="display:none;"></canvas>
    <div id="photoOutput" style="margin-top: 25px;"></div>
  </section>

  <section id="maps" style="display:none; text-align:center;">
    <h2 class="section-title">Google Maps</h2>
    <div id="map" style="max-width: 600px; height: 400px; margin: 15px auto; border-radius: 12px; border: 2px solid #0fccfc;"></div>
    <button class="back-btn" onclick="showPage('ecomView')">Back to E-commerce</button>
  </section>

</main>
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_GOOGLE_MAPS_API_KEY"></script>
<script>
  // Navigation
  function showPage(page) {
    document.querySelectorAll('main > section').forEach(s => s.style.display = 'none');
    document.getElementById(page).style.display = 'block';
    if(page === 'camera') {
      startCamera();
    }
    if(page === 'maps') {
      if(!window.mapLoaded) {
        initMap();
        window.mapLoaded = true;
      }
    }
  }
  const modules = {
    courier: ['Courier Booking', 'Ride Booking', 'Tracking', 'Support', 'Rental Vehicles'],
    job: ['Job Search', 'Post Resume', 'Local Jobs', 'Non-Local Jobs', 'PG & Hostel', 'Services Marketplace'],
    tours: ['Tour Bookings', 'Custom & Regular Tours', 'Stay Booking', 'Vehicle Booking', 'Train/Bus/Flight Tickets'],
    realestate: ['Buy', 'Sell', 'Rent', 'Key Services', 'Construction', 'Industry'],
    investment: ['Gold', 'Silver', 'Real Estate', 'Business Opportunity'],
    loans: ['Loan Enquiry', 'Car Insurance', 'Bike Insurance', 'Housing Loans', 'Personal Loans', 'Health Insurance'],
    home: ['CC Camera Installation', 'Computer Repair', 'Car Wash', 'Mobile Repair', 'Chef Services', 'Bouncers', 'Bike Mechanic', 'Car Mechanic', 'Electrician', 'Painter', 'Plumber', 'Driver']
  };
  const eventsCategories = {
    package: [
      {name: "Silver (50k -160k)", services: ["Decoration", "Catering", "DJ & Music", "Guest House", "Chocolate & Cake", "Games & Entertainment"]},
      {name: "Gold (150k - 300k)", services: ["Decoration", "Catering", "Photography", "Anchor & Actors", "Vehicles"]},
      {name: "Diamond (500k - 5M)", services: ["Premium Decoration", "Luxury Catering", "Video & Photography", "Celebrity Anchors"]},
      {name: "Platinum (500k - 800k)", services: ["Special Decoration", "Exclusive Catering", "Top DJs", "Private Guest House"]}
    ],
    customized: ["Decoration", "Catering", "Photography & Videography", "Anchor & Actors", "DJ & Singers", "Guest House", "Chocolate & Cake", "Games & Entertainment", "Jewellery", "Invitation Cards", "Vehicles", "Return Gifts", "Makeup Artist", "Mehandi Artist", "Clothing & Accessories"],
    premium: ["Decoration", "Catering", "Photography & Videography", "Anchor & Actors", "DJ & Singers", "Guest House", "Chocolate & Cake", "Games & Entertainment", "Jewellery", "Invitation Cards", "Vehicles", "Return Gifts", "Makeup Artist", "Mehandi Artist", "Clothing & Accessories"]
  };
  let currentModule = '';
  let currentService = '';
  let currentEventCategory = '';
  let currentEventService = '';
  let currentEcomCategory = '';

  function openModule(moduleName) {
    currentModule = moduleName;
    currentService = '';
    if(moduleName === 'events'){
      openEventsDashboard();
      return;
    }
    if(moduleName === 'ecommerce'){
      openEcomDashboard();
      return;
    }
    renderServiceList(modules[moduleName]);
    showPage('serviceView');
  }
  function renderServiceList(services){
    currentService = '';
    document.getElementById('serviceTitle').textContent = currentModule.charAt(0).toUpperCase() + currentModule.slice(1).replace(/_/g,' ');
    const serviceList = document.getElementById('serviceList');
    serviceList.innerHTML = '';
    services.forEach(svc => {
      let div = document.createElement('div');
      div.className = 'service-card';
      div.textContent = svc;
      div.onclick = () => openContactForm(svc);
      serviceList.appendChild(div);
    });
  }
  function openContactForm(service){
    currentService = service;
    document.getElementById('serviceList').style.display = 'none';
    document.getElementById('contactForm').style.display = 'block';
    document.getElementById('contactTitle').textContent = `Contact for ${service}`;
    clearInputs(['userName','userPhone','userMessage']);
  }
  function backToServiceList(){
    document.getElementById('contactForm').style.display = 'none';
    document.getElementById('serviceList').style.display = 'flex';
  }
  function submitContactForm(){
    let name= document.getElementById('userName').value.trim();
    let phone= document.getElementById('userPhone').value.trim();
    let message= document.getElementById('userMessage').value.trim();
    if(!name || !phone || !message){
      alert('Please fill all fields');
      return;
    }
    const whatsappUrl = `https://wa.me/8977143043?text=Name: ${encodeURIComponent(name)}%0APhone: ${encodeURIComponent(phone)}%0AMessage: ${encodeURIComponent(message)}%0AService: ${encodeURIComponent(currentService)}`;
    window.open(whatsappUrl, '_blank');
  }
  // Events & Catering functions
  function openEventsDashboard(){
    document.getElementById('dashboard').style.display = 'none';
    document.getElementById('serviceView').style.display = 'none';
    document.getElementById('ecomView').style.display = 'none';
    document.getElementById('eventsView').style.display = 'flex';
    currentEventCategory = '';
    currentEventService = '';
    const catDiv = document.getElementById('eventsCategories');
    catDiv.innerHTML = '';
    Object.keys(eventsCategories).forEach(cat => {
      let d = document.createElement('div');
      d.className = 'category-card';
      d.textContent = cat.charAt(0).toUpperCase() + cat.slice(1);
      d.onclick = () => openEventsCategory(cat);
      catDiv.appendChild(d);
    });
    document.getElementById('eventsServiceList').innerHTML = '';
    document.getElementById('eventContactForm').style.display = 'none';
    document.getElementById('eventsCategoryTitle').textContent = 'Events & Catering Categories';
  }
  function openEventsCategory(cat){
    currentEventCategory = cat;
    document.getElementById('eventsServiceList').style.display = 'flex';
    document.getElementById('eventContactForm').style.display = 'none';
    const svcList = document.getElementById('eventsServiceList');
    svcList.innerHTML = '';
    document.getElementById('eventsCategoryTitle').textContent = cat.charAt(0).toUpperCase() + cat.slice(1) + ' Services';
    if(cat === 'package'){
      eventsCategories.package.forEach(pkg => {
        let d = document.createElement('div');
        d.className = 'service-card';
        d.style.width = '260px';
        d.textContent = pkg.name;
        d.onclick = () => openPackageServices(pkg.name, pkg.services);
        svcList.appendChild(d);
      });
    } else {
      eventsCategories[cat].forEach(service => {
        let d = document.createElement('div');
        d.className = 'service-card';
        d.style.width = '200px';
        d.textContent = service;
        d.onclick = () => openEventContactForm(service, cat);
        svcList.appendChild(d);
      });
    }
  }
  function openPackageServices(pkgName, services){
    currentEventService = '';
    document.getElementById('eventsCategoryTitle').textContent = pkgName + ' Package Services';
    const svcList = document.getElementById('eventsServiceList');
    svcList.innerHTML = '';
    services.forEach(service => {
      let d = document.createElement('div');
      d.className = 'category-card';
      d.style.width = '220px';
      d.textContent = service;
      d.onclick = () => openEventContactForm(service, pkgName);
      svcList.appendChild(d);
    });
  }
  function openEventContactForm(service, cat){
    currentEventService = service;
    document.getElementById('eventsServiceList').style.display = 'none';
    const form = document.getElementById('eventContactForm');
    form.style.display = 'block';
    document.getElementById('eventsContactTitle').textContent = 'Contact for ' + service;
    document.getElementById('eventsUserName').value = '';
    document.getElementById('eventsUserPhone').value = '';
    document.getElementById('eventsUserMessage').value = '';
    document.getElementById('eventsUserName').setAttribute('data-cat', cat);
    document.getElementById('eventsUserName').setAttribute('data-serv', service);
  }
  function backToEventsCategory(){
    document.getElementById('eventContactForm').style.display = 'none';
    document.getElementById('eventsServiceList').style.display = 'flex';
  }
  function submitEventsForm() {
    const name=document.getElementById('eventsUserName').value.trim();
    const phone=document.getElementById('eventsUserPhone').value.trim();
    const message=document.getElementById('eventsUserMessage').value.trim();
    const budget=document.getElementById('eventsBudget')?.value || '';
    const capacity=document.getElementById('eventsCapacity')?.value || '';
    const cat=document.getElementById('eventsUserName').getAttribute('data-cat') || '';
    const serv=document.getElementById('eventsUserName').getAttribute('data-serv') || '';
    if(!name||!phone||!message){
      alert('Please fill all details!');
      return;
    }
    let fullMsg=`Name: ${encodeURIComponent(name)}%0APhone: ${encodeURIComponent(phone)}%0AService: ${encodeURIComponent(serv)}%0ACategory: ${encodeURIComponent(cat)}%0AMessage: ${encodeURIComponent(message)}`;
    if(budget) fullMsg += `%0ABudget: ${encodeURIComponent(budget)}`;
    if(capacity) fullMsg += `%0ACapacity: ${encodeURIComponent(capacity)}`;
    window.open(`https://wa.me/8977143043?text=${fullMsg}`, '_blank');
  }
  // E-commerce
  function openEcomDashboard(){
    document.getElementById('dashboard').style.display = 'none';
    document.getElementById('serviceView').style.display = 'none';
    document.getElementById('eventsView').style.display = 'none';
    document.getElementById('ecomView').style.display = 'flex';
    document.getElementById('ecomCategoryContent').innerHTML = '';
    document.getElementById('ecomFormSlot').innerHTML = '';
    currentEcomCategory = '';
  }
  function openEcomCategory(cat){
    currentEcomCategory = cat;
    document.getElementById('ecomCategoryContent').innerHTML = `<p style="text-align:center; font-weight:600; font-size:1.2em; margin-top:15px;">Category: ${cat}</p>`;
    showOrderForm(cat);
  }
  function showOrderForm(cat){
    const container = document.getElementById('ecomFormSlot');
    container.innerHTML = `
    <form class="contact-form" onsubmit="submitOrderForm(event, '${cat}')">
      <label>Name:</label><input type="text" name="name" required />
      <label>Mobile Number:</label><input type="tel" name="phone" maxlength="10" pattern="[6-9][0-9]{9}" required/>
      <label>Order Details:</label><textarea name="orderDetails" required></textarea>
      <label>Delivery Address:</label><textarea name="deliveryAddress" required></textarea>
      <button type="submit">Submit Order</button>
    </form>
    <button class="back-btn" onclick="openEcomDashboard()">Back to Categories</button>
    `;
  }
  function submitOrderForm(e,cat) {
    e.preventDefault();
    const form = e.target;
    const name = form.name.value.trim();
    const phone = form.phone.value.trim();
    const orderDetails = form.orderDetails.value.trim();
    const address = form.deliveryAddress.value.trim();
    if(!name || !phone || !orderDetails || !address ){
      alert('All fields are required');
      return;
    }
    const wnum = '8977143043';
    const msg = `Order from JKS E-commerce\nCategory: ${cat}\nName: ${name}\nMobile: ${phone}\nOrder Details: ${orderDetails}\nDelivery Address: ${address}`;
    window.open(`https://wa.me/${wnum}?text=${encodeURIComponent(msg)}`, '_blank');
  }
  // Profile
  function updateProfile(){
    alert('Profile updated successfully! (Placeholder action)');
  }
  // Camera functionality
  let currentStream = null;
  let usingFrontCamera = true;
  function startCamera() {
    const video = document.getElementById('video');
    if(currentStream) {
      currentStream.getTracks().forEach(track => track.stop());
    }
    const constraints = { video: { facingMode: usingFrontCamera ? 'user' : 'environment' } };
    navigator.mediaDevices.getUserMedia(constraints)
      .then(stream => {
        currentStream = stream;
        video.srcObject = stream;
      })
      .catch(err => alert('Camera access denied or unavailable.'));
  }
  function switchCamera() {
    usingFrontCamera = !usingFrontCamera;
    startCamera();
  }
  function capturePhoto() {
    const video = document.getElementById('video');
    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');
    canvas.width = video.videoWidth;
    canvas.height = video.videoHeight;
    ctx.drawImage(video, 0, 0);
    const imgData = canvas.toDataURL('image/png');
    const photoOutput = document.getElementById('photoOutput');
    photoOutput.innerHTML = `<img src="${imgData}" style="max-width:100%; border-radius: 10px; margin-top:15px;" alt="Captured photo">`;
  }
  function initMap() {
    const center = {lat: 17.3850, lng: 78.4867};
    const map = new google.maps.Map(document.getElementById('map'), {center: center, zoom: 12});
  }
  document.addEventListener('DOMContentLoaded', () => {
    showPage('dashboard');
  });
</script>
<script async defer src="https://maps.googleapis.com/maps/api/js?key=YOUR_GOOGLE_MAPS_API_KEY&callback=initMap"></script>
</body>
</html>
