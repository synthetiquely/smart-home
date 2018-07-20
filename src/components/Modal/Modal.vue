<template>
  <transition name="modal">
    <div class="backdrop">
      <div class="modal">
        <div class="modal__container">
          <div class="modal__header">
            <slot name="header"/>
          </div>
          <div class="modal__content">
            <slot name="content"/>
          </div>
        </div>
        <div class="modal__footer">
          <slot name="footer"/>
        </div>
      </div>
    </div>
  </transition>
</template>

<style scoped>
.backdrop {
  position: fixed;
  z-index: 200;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(51, 51, 51, 0.5);
  transition: opacity 0.3s ease;
}

.modal {
  position: fixed;
  z-index: 201;
  top: 50%;
  left: 50%;
  width: 630px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transform: translate(-50%, -50%);
  transition: all 0.3s ease;
  background-color: transparent;
}

.modal__container {
  width: calc(100% - 30px);
  height: 208px;
  margin-bottom: 20px;
  padding: 15px;
  display: flex;
  flex-direction: column;
  background-color: var(--white);
  border-radius: 20px;
}

.modal__header {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal,
.modal-leave-active .modal {
  transform: scale(1.1);
}
</style>
