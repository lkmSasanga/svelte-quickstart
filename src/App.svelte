<script>
  import Product from "./Product.svelte";

  let title = "";
  let price = 0;
  let description = "";

  function setTitle(event) {
    title = event.target.value;
  }
</script>

<p>{title}</p>

<section>
  <div>
    <label for="title">Title</label>
    <input type="text" id="title" value={title} on:input={setTitle} />
  </div>
  <div>
    <label for="price">Price</label>
    <input type="number" id="price" />
  </div>
  <div>
    <label for="description">Description</label>
    <input rows="3" id="description" />
  </div>
</section>

<Product />

<style>
  section {
    width: 30rem;
    margin: auto;
  }
  label,
  input,
  textarea {
    width: 100%;
  }
</style>
