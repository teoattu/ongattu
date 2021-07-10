<script>
import { createEventDispatcher } from "svelte";


  export let isOpen = false;

  const dispatch = createEventDispatcher();

  const onClose = () => {
    isOpen = false;
    dispatch('change', {
      isOpen: false
    })
  }

</script>

{#if isOpen}
  <div
    class="modal"
    on:blur={() => {
      isOpen = false;
    }}
  >
    <div class="modal__content">
      <button class="modal__close" on:click={onClose} role="button">
        <svg
          class="w-6 h-6"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
          ><path
            fill-rule="evenodd"
            d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z"
            clip-rule="evenodd"
          /></svg
        >
      </button>
      <slot />
    </div>
  </div>
{/if}

<style lang="scss">
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    z-index: 102;
    padding: 20px;
    &__content {
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 40px;
      background: #fff;
      font-size: 16px;
      border-radius: 4px;
      box-shadow: 0 3px 7px rgba(0, 0, 0, 0.3);
      -webkit-background-clip: padding-box;
      -moz-background-clip: padding-box;
      background-clip: padding-box;
      max-width: 70%;
      max-height: 80%;
      overflow: auto;
      @media (min-width: 1024px) {
        font-size: 18px;
      }
    }

    &__close {
      position: absolute;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      top: 0;
      right: 0;
      padding: 10px;
      margin-bottom: 10px;
      border: none;
      border-top-right-radius: 4px;
      color: var(--ultralight-blue-color);
      background-color: transparent;
      cursor: pointer;
      transition: all 150ms ease-in-out;

      svg {
        width: 20px;
        height: 20px;
      }

      &:hover {
        color: var(--blue-color);
      }
    }
  }
</style>
