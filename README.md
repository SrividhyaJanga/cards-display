<!DOCTYPE html>
<html>
    <head>
        <title>chards</title>
    </head>
    <body>
      <style>
          .card {
  border: 1px solid rgb(183, 177, 177);
  border-radius: 1px;
  padding: 10px;
  margin: 30px 0px 50px 550px;
  width: 200px;
  height: 100px;
  display: flex;
  text-align: center;
  background-color: blanchedalmond;
}
#db{
  color: aqua;
  background-color: black;
  padding: 50px;
  margin: 100px 500px 50px 500px;
  font-size: 25px;
}

      </style>
        <button id="db">press on the button</button>
        <div id="cardContainer"></div>
    <script>
const data = [
  { content: '1.account number <br> 2.transaction' },
  { content: '3.pin generation <br> 4.balance check' }
];
function createCards() {
  const cardContainer = document.getElementById('cardContainer');
  cardContainer.innerHTML = '';

  data.forEach(item => {
    const card = document.createElement('div');
    card.classList.add('card');
    card.innerHTML = `
      <h2><b>${item.content}</b></h2>
    `
    cardContainer.appendChild(card);
  });
}

document.getElementById('db').addEventListener('click', function() {
  createCards();
  const cards = document.querySelectorAll('.card');
  cards.forEach(card => {
    card.style.display = 'block';
  });
});
    </script>
    </body>
</html>
