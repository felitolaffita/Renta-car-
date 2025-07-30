<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Renta de Autos - Tu Viaje Seguro</title>
  <style>
    body {
      margin: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f7f7f7; color: #222;
      display: flex; flex-direction: column; min-height: 100vh;
    }
    header {
      background: #111; color: #fff; padding: 1.5rem; text-align: center;
    }
    nav {
      background: #222; display: flex; justify-content: center; gap: 2rem;
      padding: 1rem;
    }
    nav a {
      color: white; text-decoration: none; font-weight: 600;
      transition: color 0.3s;
    }
    nav a:hover {
      color: #0af;
    }
    main {
      flex-grow: 1; max-width: 900px; margin: 2rem auto; padding: 0 1rem;
    }
    h2 {
      text-align: center; margin-bottom: 1.5rem; color: #111;
    }
    .cars-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.5rem;
    }
    .car-card {
      background: white; border-radius: 10px; box-shadow: 0 4px 10px rgb(0 0 0 / 0.1);
      overflow: hidden; display: flex; flex-direction: column;
    }
    .car-card img {
      width: 100%; height: 160px; object-fit: cover;
    }
    .car-card-content {
      padding: 1rem; flex-grow: 1;
    }
    .car-card-content h3 {
      margin: 0 0 0.5rem 0;
      color: #111;
    }
    .car-card-content p {
      margin: 0 0 1rem 0;
      color: #444;
    }
    .btn-whatsapp {
      display: inline-block; background: #25d366; color: white; padding: 0.6rem 1rem;
      border-radius: 5px; text-decoration: none; font-weight: 600; transition: background 0.3s;
    }
    .btn-whatsapp:hover {
      background: #1ebe57;
    }
    form {
      background: white; padding: 1.5rem; border-radius: 10px;
      box-shadow: 0 4px 10px rgb(0 0 0 / 0.1); max-width: 400px; margin: 2rem auto;
    }
    form label {
      display: block; margin-bottom: 0.3rem; font-weight: 600;
    }
    form input, form select, form textarea {
      width: 100%; padding: 0.5rem; margin-bottom: 1rem; border-radius: 5px;
      border: 1px solid #ccc; font-size: 1rem;
    }
    form button {
      background: #111; color: white; border: none; padding: 0.7rem 1.2rem;
      font-size: 1rem; border-radius: 5px; cursor: pointer;
      transition: background 0.3s;
    }
    form button:hover {
      background: #444;
    }
    footer {
      background: #111; color: white; text-align: center; padding: 1.5rem;
      margin-top: auto;
    }
    .payments {
      display: flex; justify-content: center; gap: 2rem; margin-top: 2rem;
    }
    .payments img {
      width: 60px; filter: drop-shadow(0 0 2px rgba(0,0,0,0.3));
    }

    @media (max-width: 500px) {
      nav {
        flex-direction: column;
        gap: 1rem;
      }
      .payments {
        flex-wrap: wrap;
        gap: 1rem;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>Renta de Autos - Tu Viaje Seguro</h1>
  <nav>
    <a href="#autos">Autos</a>
    <a href="#reserva">Reserva</a>
    <a href="#contacto">Contacto</a>
  </nav>
</header>

<main>
  <section id="autos">
    <h2>Autos Disponibles</h2>
    <div class="cars-grid">
      <div class="car-card">
        <img src="https://images.unsplash.com/photo-1571607387152-1f1e06e9ccfe" alt="BMW Serie 5">
        <div class="car-card-content">
          <h3>BMW Serie 5</h3>
          <p>Desde $90/día</p>
          <a href="https://wa.me/5363620747?text=Hola%20quiero%20rentar%20el%20BMW%20Serie%205" target="_blank" class="btn-whatsapp">WhatsApp</a>
        </div>
      </div>
      <div class="car-card">
        <img src="https://images.unsplash.com/photo-1601158935945-0c7e3df8c8e9" alt="Range Rover Evoque">
        <div class="car-card-content">
          <h3>Range Rover Evoque</h3>
          <p>Desde $120/día</p>
          <a href="https://wa.me/5363620747?text=Hola%20quiero%20rentar%20el%20Range%20Rover%20Evoque" target="_blank" class="btn-whatsapp">WhatsApp</a>
        </div>
      </div>
      <div class="car-card">
        <img src="https://images.unsplash.com/photo-1589391886647-4e6d04e994f7" alt="Ford Mustang">
        <div class="car-card-content">
          <h3>Ford Mustang</h3>
          <p>Desde $150/día</p>
          <a href="https://wa.me/5363620747?text=Hola%20quiero%20rentar%20el%20Ford%20Mustang" target="_blank" class="btn-whatsapp">WhatsApp</a>
        </div>
      </div>
    </div>
  </section>

  <section id="reserva">
    <h2>Reserva tu Auto</h2>
    <form id="reservaForm">
      <label for="nombre">Nombre Completo</label>
      <input type="text" id="nombre" name="nombre" required />

      <label for="email">Correo Electrónico</label>
      <input type="email" id="email" name="email" required />

      <label for="auto">Auto</label>
      <select id="auto" name="auto" required>
        <option value="">Selecciona un auto</option>
        <option value="BMW Serie 5">BMW Serie 5</option>
        <option value="Range Rover Evoque">Range Rover Evoque</option>
        <option value="Ford Mustang">Ford Mustang</option>
      </select>

      <label for="metodoPago">Método de Pago</label>
      <select id="metodoPago" name="metodoPago" required>
        <option value="">Selecciona método</option>
        <option value="Tarjeta de crédito">Tarjeta de crédito</option>
        <option value="PayPal">PayPal</option>
        <option value="Transferencia bancaria">Transferencia bancaria</option>
      </select>

      <label for="mensaje">Mensaje adicional</label>
      <textarea id="mensaje" name="mensaje" rows="3"></textarea>

      <button type="submit">Enviar Reserva</button>
    </form>
  </section>

  <section id="contacto" style="text-align:center; margin-top:3rem;">
    <h2>Contacto</h2>
    <p>📞 Llámanos o escríbenos por WhatsApp: <a href="https://wa.me/5363620747" target="_blank" style="color:#25d366; font-weight:700;">+53 6362 0747</a></p>
    <div class="payments" aria-label="Métodos de pago aceptados">
      <img src="https://upload.wikimedia.org/wikipedia/commons/0/04/Visa.svg" alt="Visa" />
      <img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg" alt="PayPal" />
      <img src="https://upload.wikimedia.org/wikipedia/commons/5/57/Mastercard_logo.svg" alt="Mastercard" />
      <img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/Bank_transfer_icon.svg" alt="Transferencia bancaria" />
    </div>
  </section>
</main>

<footer>
  <p>&copy; 2025 Renta de Autos - Tu Viaje Seguro</p>
</footer>

<script>
  // Simulación de envío de formulario
  document.getElementById('reservaForm').addEventListener('submit', function(e){
    e.preventDefault();
    alert('Gracias por tu reserva, nos pondremos en contacto contigo pronto.');
    this.reset();
  });
</script>

</body>
</html>
