<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <li
      v-for="transaction in transactions"
      :key="transaction.id"
      :class="transaction.amount < 0 ? 'minus' : 'plus'">
      {{ transaction.text }} <span>${{ transaction.amount }}</span>
      <button class="delete-btn">❌</button>
    </li>
  </ul>
</template>

//Using 'setup' in the script tag, is a quicker way of using the setup function. User does not have to explicity call the setup function and return the variable of the setup function. 
<script setup>
    const transactions = [
      { id: 1, text: 'Flower', amount: -19.99 },
      { id: 2, text: 'Salary', amount: 299.97 },
      { id: 3, text: 'Book', amount: -10 },
      { id: 4, text: 'Camera', amount: -150 },
    ];
</script>
