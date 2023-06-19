<script>
	import Button from "./Button.svelte";


  const handleSubmit = (e) => {
    e.preventDefault()

    console.log(e.target.elements)
  }
</script>
<form class="form" on:submit={handleSubmit}>
  <input type="text" name="name" id="" placeholder="Your Name" required>
  <input type="email" name="email" id="" placeholder="Your Email" required>
  <input type="tel" name="phone" id="" placeholder="Yuor phone" required>
  <textarea placeholder="Your message" name="message" rows={10}></textarea>
  <Button type="submit" class="submit-btn">Send message</Button>
</form>

<style>
  .form {
    background-color: var(--primary100);
    padding: 2rem 1rem;
    box-shadow: rgba(0, 0, 0, .25);
  }

  input {
    width: 100%;
    margin-bottom: 1.75rem;
    padding: .75rem 1rem;
    background-color: var(--primary);
    border: 1px solid #555;
    color: #fff;
    outline: 0;
  }

  textarea {
    width: 100%;
    background-color: var(--primary);
    border: 1px solid #555;
    color: #fff;
    padding: .75rem 1rem;
    resize: none;
    outline: 0;
    margin-bottom: 1.75rem;
  }

  input:focus, textarea:focus {
    border-color: #ccc;
  }

  .form :global(.submit-btn) {
    text-transform: uppercase;
    width: 15rem
  }
</style>