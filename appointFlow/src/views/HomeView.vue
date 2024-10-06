<template>
  <div class="home">
    <header>
      <h1>AppointFlow</h1>
      <p class="tagline">Место где поток клиентов течет плавно, а записи не утекают!</p>
    </header>
    <main>
      <section class="features">
        <h2>Возможности</h2>
        <ul>
          <li>Простое управление записями</li>
          <li>Ведение истории клиентов</li>
          <li>Гибкое расписание</li>
          <li>Напоминания и уведомления</li>
        </ul>
      </section>
    </main>
    <footer>
      <p>&copy; 2023 AppointFlow. Все права защищены.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>

<style scoped>
.home {
   font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  color: #333;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  flex-grow: 1;
}

header {
  text-align: center;
  margin-bottom: 40px;
}

h1 {
  color: #2c3e50;
  font-size: 3em;
  margin-bottom: 10px;
}

.tagline {
  font-size: 1.2em;
  color: #7f8c8d;
}

.features {
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  margin-bottom: 30px;
}

.features h2 {
  color: #2c3e50;
  margin-bottom: 15px;
}

.features ul {
  list-style-type: none;
  padding: 0;
}

.features li {
  margin-bottom: 10px;
  padding-left: 20px;
  position: relative;
}

.features li::before {
  content: '✓';
  color: #27ae60;
  position: absolute;
  left: 0;
}

.actions {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 40px;
}

.btn {
  padding: 10px 20px;
  font-size: 1em;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.btn.primary {
  background-color: #3498db;
  color: white;
}

.btn.primary:hover {
  background-color: #2980b9;
}

.btn.secondary {
  background-color: #ecf0f1;
  color: #2c3e50;
}

.btn.secondary:hover {
  background-color: #bdc3c7;
}

footer {
  margin-top: auto;
  text-align: center;
  color: #7f8c8d;
  font-size: 0.9em;
  padding: 20px 0;
}
</style>
