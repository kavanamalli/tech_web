<script>
  let contacts = [
    { category: "Admission Office", phone: "+91 80 22167929", fax: "" },
    { category: "College EPABX", phone: "+91 80 22167805", fax: "" },
    { category: "General Inquiries", phone: "+91 80 22167800/8969", fax: "" }
  ];
</script>

<div class="contact-container">
  <h1>Contact Us</h1>

  <!-- Grid Layout -->
  <div class="contact-grid">
    
    <!-- Contact Address -->
    <div class="address">
      <h2>📍 Campus Address</h2>
      <p><strong>Nitte Meenakshi Institute of Technology</strong></p>
      <p>P.B No 6429, Yelahanka, Bangalore - 560064, Karnataka, India</p>
      <p>📞 <strong>+91-81500-04555</strong></p>
      <p>📧 <a href="mailto:enquiry@nitte.edu.in">enquiry@nitte.edu.in</a></p>
    </div>

    <!-- Contact Table -->
    <div class="contact-table">
      <h2>📞 Campus Contacts</h2>
      <table>
        <thead>
          <tr>
            <th>Department</th>
            <th>Phone</th>
          </tr>
        </thead>
        <tbody>
          {#each contacts as contact}
            <tr>
              <td>{contact.category}</td>
              <td>{contact.phone}</td>
            </tr>
          {/each}
        </tbody>
      </table>
    </div>

  </div>

  <!-- Google Map -->
  <div class="map-container">
    <h2>📍 Find Us on Map</h2>
    <iframe
  title="Location Map"
  src="https://www.google.com/maps/embed?...your_map_url..."
  width="100%" 
  height="350" 
  style="border:0;" 
  allowfullscreen="" 
  loading="lazy">
</iframe>
  </div>
</div>

<style>
  .contact-container {
    padding: 40px;
    max-width: 1100px;
    margin: auto;
  }

  h1 {
    text-align: center;
    color: #007bff;
    font-size: 2.5rem;
    margin-bottom: 20px;
  }

  .contact-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .address, .contact-table {
    flex: 1;
    min-width: 300px;
    padding: 20px;
    background: #f8f9fa;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .address {
    margin-right: 20px;
  }

  h2 {
    color: #0056b3;
    font-size: 1.8rem;
    margin-bottom: 10px;
  }

  p {
    font-size: 1.1rem;
    color: #333;
    margin-bottom: 5px;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 10px;
  }

  th, td {
    border: 1px solid #ddd;
    padding: 10px;
    text-align: left;
  }

  th {
    background: #007bff;
    color: white;
  }

  td {
    background: white;
  }

  /* Map */
  .map-container {
    margin-top: 30px;
    text-align: center;
  }

  iframe {
    border-radius: 10px;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .contact-grid {
      flex-direction: column;
    }

    .address {
      margin-right: 0;
      margin-bottom: 20px;
    }
  }
</style>
