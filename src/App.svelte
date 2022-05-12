<script>
  import Product from "./Product.svelte";
  import Button from './Button.svelte'

  let title = "";
  let price = 0;
  let description = "";

  function setTitle(event) {
    title = event.target.value;
  }
</script>

<section>
  <div>
    <label for="title">Title</label>
    <input type="text" id="title" value={title} on:input={setTitle} />
  </div>
  <div>
    <label for="price">Price</label>
    <input type="number" id="price" bind:value={price} />
  </div>
  <div>
    <label for="description">Description</label>
    <input rows="3" id="description" bind:value={description} />
  </div>

  <Button>Create product</Button>
</section>

<Product
  productTitle={title}
  productPrice={price}
  productDescription={description}
/>

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
