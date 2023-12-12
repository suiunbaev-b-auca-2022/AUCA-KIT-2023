<!-- /routes/contacts/+page.svelte -->

<script>
  export let name = "Baitur Suiunbaev";
  export let organization = "BS Company";
  export let address = "123 Main Street, Suite 456 Cityville, State 78901";
  export let phone = "+996771234567";
  export let email = "contact@mywebsite.com";
  export let operatingHours = {
    weekdays: "Monday - Friday: 9:00 AM - 5:00 PM",
    saturday: "Saturday: 10:00 AM - 2:00 PM",
    sunday: "Sunday: Closed",
  };
  export let customerSupport = {
    email: "support@mywebsite.com",
    phone: "+996 (771) 234567",
  };
  export let salesDepartment = {
    email: "sales@mywebsite.com",
    phone: "+996 (770) 123456",
  };
</script>

<main>
  <h2 id="contacts1">Contacts</h2>
  <p>Name: {name}</p>
  <p>Organization: {organization}</p>
  <p>Address: {address}</p>
  <p>Phone: {phone}</p>
  <p>Email: {email}</p>

  <h4>Operating Hours:</h4>
  <p>{operatingHours.weekdays}</p>
  <p>{operatingHours.saturday}</p>
  <p>{operatingHours.sunday}</p>

  <h4>Customer Support:</h4>
  <p>Email: {customerSupport.email}</p>
  <p>Phone: {customerSupport.phone}</p>

  <h4>Sales Department:</h4>
  <p>Email: {salesDepartment.email}</p>
  <p>Phone: {salesDepartment.phone}</p>
</main>
