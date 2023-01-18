<div id="text"></div>

<script>
  fetch('https://api.github.com/orgs/nodejs', {
    headers: new Headers({
      'User-agent': 'Mozilla/4.0 Custom User Agent'
    })
  })
  .then(response => response.json())
  .then(data => {
    console.log(data)
    document.getElementById("text").innerHTML = data;
  })
  .catch(error => console.error(error))
</script>
