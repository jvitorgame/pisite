document.addEventListener('DOMContentLoaded', function() {
  const form = document.getElementById('contactForm');
  const successMessage = document.getElementById('successMessage');
  const errorMessage = document.getElementById('errorMessage');

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    // Clear previous messages
    successMessage.style.display = 'none';
    errorMessage.style.display = 'none';

    const formData = new FormData(form);
    const name = formData.get('name');
    const email = formData.get('email');
    const message = formData.get('message');

    // Validate form data
    if (!name || !email || !message) {
      errorMessage.textContent = 'Por favor, preencha todos os campos.';
      errorMessage.style.display = 'block';
      return;
    }

    if (!validateEmail(email)) {
      errorMessage.textContent = 'Por favor, insira um e-mail válido.';
      errorMessage.style.display = 'block';
      return;
    }

    // Simulate form submission (you can replace this with an actual server call)
    console.log('Form submitted:', { name, email, message });

    // Clear the form
    form.reset();

    // Show success message
    successMessage.style.display = 'block';
    successMessage.textContent = 'Mensagem enviada com sucesso! Entraremos em contato em breve.';
  });

  // Function to validate email format
  function validateEmail(email) {
    const emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;
    return emailPattern.test(email);
  }
});
