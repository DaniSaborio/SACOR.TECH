<style scoped>
  .container {
    width: 100%;
    height: 100%;
    --s: 200px;
    --c1: #1d1d1d;
    --c2: #4e4f51;
    --c3: #3c3c3c;

    background:
      repeating-conic-gradient(
          from 30deg,
          #0000 90deg 120deg,
          var(--c3) 0deg 180deg
        )
        calc(0.5 * var(--s)) calc(0.5 * var(--s) * 0.577),
      repeating-conic-gradient(
        from 30deg,
        var(--c1) 0deg 60deg,
        var(--c2) 0deg 120deg,
        var(--c3) 0deg 180deg
      );
    background-size: var(--s) calc(var(--s) * 0.577);
  }
  .container{
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  min-width: 100%;
  min-height: 100%;
  z-index: -1; /* Estará detrás del resto */
  /* Resto de tu estilo ... */
  background-color: #05050a;
  overflow: hidden;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(40px, 1fr));
  grid-auto-rows: 40px;
  font-size: 32px;
  color: rgba(0, 150, 255, 0.4);
  font-family: "Courier New", Courier, monospace;
  justify-content: center;
  align-content: center;
}
</style>

<template>
  <div class="container"></div>
</template>
