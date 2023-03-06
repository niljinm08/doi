# doi
doi
const form = document.querySelector('form');
const searchInput = document.querySelector('#search');

form.addEventListener('submit', (e) => {
  e.preventDefault();
  const searchTerm = searchInput.value;
  fetch('/doi-finder.php?search=' + searchTerm)
    .then(response => response.json())
    .then(data => {
      // Parse the JSON data and display the DOIs to the user
    })
    .catch(error => {
      console.error(error);
    });
});
