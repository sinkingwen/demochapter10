<!-- <template>
  <div class="card-box">
    <h2>卡片</h2>
    <div>
      <slot></slot>
    </div>
  </div>
</template> -->

<template>
  <div class="card-box">
    <header>
      <slot name="header"></slot>
    </header>
    <main>
      <slot>default</slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>