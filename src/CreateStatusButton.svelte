<style>
  @-webkit-keyframes ripple {
    0% {
      width: 0;
      height: 0;
      opacity: 0.5;
    }
    100% {
      width: 150px;
      height: 150px;
      opacity: 0;
    }
  }

  @keyframes ripple {
    0% {
      width: 0;
      height: 0;
      opacity: 0.5;
    }
    100% {
      width: 150px;
      height: 150px;
      opacity: 0;
    }
  }
  .ripple:before {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    -webkit-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
    border-radius: 50%;
    background-color: currentColor;
    visibility: hidden;
    z-index: 2;
  }
  .ripple:not(:active):before {
    -webkit-animation: ripple 0.4s cubic-bezier(0, 0, 0.2, 1);
    animation: ripple 0.4s cubic-bezier(0, 0, 0.2, 1);
    -webkit-transition: visibility 0.4s step-end;
    transition: visibility 0.4s step-end;
  }
  .ripple:active:before {
    visibility: visible;
  }
  main {
    position: fixed;
    bottom: 5rem;
    right: 1.2rem;
  }
  .icon {
    border-radius: 100%;
    background: rgb(19, 102, 255);
    height: 3.4rem;
    width: 3.4rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  svg {
    color: rgb(236, 236, 236);
    width: 1.8rem;
    height: 1.8rem;
  }
</style>

<main>
  <div class="icon ripple">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 24 24"
      fill="none"
      stroke="currentColor"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
      class="feather feather-plus">
      <line x1="12" y1="5" x2="12" y2="19" />
      <line x1="5" y1="12" x2="19" y2="12" />
    </svg>
  </div>
</main>
