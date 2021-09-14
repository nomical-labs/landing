<script>
  export let title
  export let description
  export let link
  export let logo
  export let end
  export let disabled
  let style = ''

  if (disabled) style = style + 'cursor: no-drop; background: rgb(216, 216, 216)'
  if (end) style = style + 'width: 50%; margin: auto;'
</script>
<style>
  .flex-column {
    flex-direction: column;
  }

  .item {
    border: 2px solid rgb(216, 216, 216);
    border-radius: 8px;
    padding: 0rem 0.4rem;
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
  }
  .item > img {
    width: 50px;
    height: 50px;
    padding-right: 1rem;
  }
  .item > div > h3 {
    margin: 0;
    padding: 0.3rem 0 0.2rem 0;
  }
  .item > div > p {
    margin: 0;
    font-size: 12px;
    color: #919191;
    padding-bottom: 0.4rem;
  }
  .item > div {
    padding-right: 0.4rem;
  }
  @media only screen and (min-width: 700px) {
    .item {
      width: auto;
    }
  }
</style>

<a href={link} target="_black">
  <div class="item" style="{style}">
    <img src={logo} alt={title + ' logo'}>
    <div class="flex flex-column">
      <h3>{title}</h3>
      <p>{description}</p>
    </div>
  </div>
</a>