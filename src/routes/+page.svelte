<script>
    export let data;
</script>

<div class="overflow-x-auto">
    <table class="table">
      <!-- head -->
      <thead>
        <tr>
          <th>
            <label>
              <input type="checkbox" class="checkbox" />
            </label>
          </th>
          <th>Product</th>
          <th>Description</th>
          <th>Price</th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <!-- row 1 -->
         {#each data.products as product}
         <tr>
            <th>
              <label>
                <input type="checkbox" class="checkbox" />
              </label>
            </th>
            <td>
              <div class="flex items-center gap-3">
                <div class="avatar">
                  <div class="mask mask-squircle h-12 w-12">
                    <img
                      src={product.thumbnail}
                      alt="Avatar Tailwind CSS Component" />
                  </div>
                </div>
                <div>
                  <div class="font-bold">{product.title}</div>
                  <div class="text-sm opacity-50">{product.category}</div>
                </div>
              </div>
            </td>
            <td>
              {product.description}
              <br />
              <span class="badge badge-ghost badge-sm">{product.warrantyInformation}</span>
            </td>
            <td><strong>{product.price} $</strong></td>
            <th>
              <button class="btn btn-info">Buy</button>
            </th>
          </tr>
         {/each}
      </tbody>
      <!-- foot -->
      <tfoot>
        <tr>
          <th></th>
          <th>Product</th>
          <th>Description</th>
          <th>Price</th>
          <th></th>
        </tr>
      </tfoot>
    </table>
  </div>

<!-- <h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<strong>20240913 08:44 Test OK</strong>
<br>
<a class="btn btn-primary" href="/contacts">Contacts</a> -->