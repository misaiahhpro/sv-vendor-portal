<script>
  import successkid from 'images/successkid.jpg';
  import { files } from '../stores/FileStore';

  let fileArray;

  const unsubscribe = files.subscribe((value) => {
    fileArray = value;
  });
</script>

<svelte:head>
  <title>Vendor Portal</title>
</svelte:head>

<h1>Login<span class='test'>test</span></h1>
<div>{fileArray.length}</div>

<style lang="scss">
  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
      .test {
        background-color: green;
      }
    }
  }
</style>
