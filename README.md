# Botão Flutuante de WhatsApp (HTML + CSS + JavaScript)

Este projeto adiciona um **botão flutuante de WhatsApp** a um site institucional, permitindo que visitantes entrem em contato rapidamente com uma mensagem pré-preenchida.

## ✨ Funcionalidades

- 📍 Fica **fixo no canto inferior direito**
- 📱 Funciona em **desktop e mobile**
- 💬 Abre o WhatsApp com **mensagem automática**
- 🎬 Possui **animação suave** para chamar atenção
- 🧩 Desenvolvido com **HTML, CSS e JavaScript puros**
- ♻️ Fácil de reutilizar em outros projetos

---

## 🧩 1. HTML

Adicione o código abaixo **antes do `</body>`** no arquivo `index.html`:

```html
<!-- Botão flutuante WhatsApp -->
<a
  href="https://wa.me/5599999999999?text=Oi%2C%20gostaria%20de%20agendar%20uma%20avalia%C3%A7%C3%A3o%20com%20o%20Dr.%20Pedro."
  class="whatsapp-float"
  target="_blank"
  aria-label="Falar no WhatsApp"
>
  <span class="whatsapp-text">Agendar pelo WhatsApp</span>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 32 32"
    class="whatsapp-icon"
  >
    <path
      fill="currentColor"
      d="M16.04 2.01C8.34 2.01 2.1 8.25 2.1 15.95c0 2.78.81 5.39 2.21 7.6L2 30l6.64-2.24c2.13 1.17 4.6 1.84 7.4 1.84 7.7 0 13.94-6.24 13.94-13.94S23.74 2.01 16.04 2.01zm0 24.64c-2.38 0-4.6-.7-6.47-1.9l-.46-.29-3.94 1.33 1.28-3.84-.3-.49a10.67 10.67 0 01-1.67-5.73c0-5.9 4.8-10.7 10.7-10.7s10.7 4.8 10.7 10.7-4.8 10.7-10.7 10.7zm6.01-8.23c-.33-.17-1.95-.96-2.25-1.07-.3-.11-.52-.17-.74.17-.22.33-.85 1.07-1.04 1.29-.19.22-.39.25-.72.08-.33-.17-1.39-.51-2.65-1.62-.98-.88-1.64-1.96-1.83-2.29-.19-.33-.02-.51.15-.68.15-.15.33-.39.5-.59.17-.19.22-.33.33-.56.11-.22.06-.42-.03-.59-.08-.17-.74-1.78-1.02-2.44-.27-.64-.55-.55-.74-.56-.19-.01-.42-.01-.64-.01s-.59.08-.9.42c-.31.33-1.18 1.15-1.18 2.81s1.21 3.26 1.38 3.48c.17.22 2.38 3.63 5.76 5.09.8.35 1.43.56 1.92.72.81.26 1.55.22 2.13.13.65-.1 1.95-.8 2.23-1.57.28-.77.28-1.43.19-1.57-.08-.14-.3-.22-.63-.39z"
    />
  </svg>
</a>
```
📌 Importante

Substitua o número 5599999999999 pelo WhatsApp real

---

## 🧩 2. CSS

```CSS
/* Botão flutuante WhatsApp */
.whatsapp-float {
  position: fixed;
  bottom: 20px;
  right: 20px;
  display: flex;
  align-items: center;
  gap: 0.6rem;
  padding: 0.7rem 1.1rem;
  background-color: #25d366;
  color: #fff;
  border-radius: 999px;
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 500;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.25);
  z-index: 9999;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.whatsapp-float:hover {
  transform: translateY(-3px);
  box-shadow: 0 12px 26px rgba(0, 0, 0, 0.3);
}

.whatsapp-icon {
  width: 22px;
  height: 22px;
}

/* Texto aparece apenas no desktop */
.whatsapp-text {
  display: none;
}

@media (min-width: 768px) {
  .whatsapp-text {
    display: inline;
  }
}
```

---

## 🧩 3. JAVA SCRIPT

Esse script adiciona uma animação suave de entrada e pode ser reutilizado futuramente para eventos de analytics.

Adicione no arquivo script.js:

```Java Script

// Animação de entrada do botão WhatsApp
document.addEventListener("DOMContentLoaded", () => {
  const whatsappBtn = document.querySelector(".whatsapp-float");

  whatsappBtn.style.opacity = "0";
  whatsappBtn.style.transform = "translateY(20px)";

  setTimeout(() => {
    whatsappBtn.style.transition = "opacity 0.4s ease, transform 0.4s ease";
    whatsappBtn.style.opacity = "1";
    whatsappBtn.style.transform = "translateY(0)";
  }, 300);
});
```

---

✅ Resultado Final

✔ Botão sempre visível
✔ Design profissional e discreto
✔ Totalmente responsivo
✔ Código simples e reutilizável
✔ Ideal para sites institucionais e pequenos negócios

---

## 🧩 4. LICENÇA

Uso livre para projetos pessoais, acadêmicos ou comerciais.
