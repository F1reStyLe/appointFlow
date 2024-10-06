<template>
  <div class="appointment-form">
    <h2>Запись на прием</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Имя:</label>
        <input type="text" id="name" v-model="form.name" required>
      </div>
      
      <div class="form-group">
        <label for="phone">Телефон:</label>
        <input
          type="tel"
          id="phone"
          v-model="form.phone"
          v-mask="'#-(###)-###-##-##'"
          required
        >
      </div>
      
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="form.email" required>
      </div>
      
      <div class="form-group">
        <label for="service">Услуга:</label>
        <select id="service" v-model="form.service" required>
          <option value="">Выберите услугу</option>
          <option value="haircut">Стрижка</option>
          <option value="coloring">Окрашивание</option>
          <option value="manicure">Маникюр</option>
          <option value="pedicure">Педикюр</option>
        </select>
      </div>
      
      <div class="form-group">
        <label for="date">Дата:</label>
        <input type="date" id="date" v-model="form.date" required>
      </div>
      
      <div class="form-group">
        <label for="time">Время:</label>
        <input type="time" id="time" v-model="form.time" required>
      </div>
      
      <div class="form-group">
        <label for="notes">Дополнительные пожелания:</label>
        <textarea id="notes" v-model="form.notes"></textarea>
      </div>
      
      <button type="submit" class="submit-btn">Записаться</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'ClientAppointmentForm',
  data() {
    return {
      form: {
        name: '',
        phone: '',
        email: '',
        service: '',
        date: '',
        time: '',
        notes: ''
      }
    }
  },
  methods: {
    submitForm() {
      // Здесь будет логика отправки формы
      console.log('Форма отправлена:', this.form);
      // В реальном приложении здесь будет запрос к API для сохранения данных
      // Также можно добавить валидацию перед отправкой
      
      // Очистка формы после отправки
      this.form = {
        name: '',
        phone: '',
        email: '',
        service: '',
        date: '',
        time: '',
        notes: ''
      };
    }
  }
}
</script>

<style scoped>
.appointment-form {
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f8f9fa;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h2 {
  text-align: center;
  color: #2c3e50;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
  color: #34495e;
}

input[type="text"],
input[type="tel"],
input[type="email"],
input[type="date"],
input[type="time"],
select,
textarea {
  width: 100%;
  padding: 8px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 16px;
}

textarea {
  height: 100px;
  resize: vertical;
}

.submit-btn {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #3498db;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.submit-btn:hover {
  background-color: #2980b9;
}
</style>
