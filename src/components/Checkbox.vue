<template>
  <div class="checkbox">
    <input type="checkbox" name="check" id="check" class="checkbox__checkbox" />
    <label class="checkbox__label" for="check">{{msg}}</label>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Checkbox extends Vue {
  @Prop() private msg!: string;
}
</script>

<style scoped lang="scss">
.checkbox {
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  color: #aaaaaa;
}

.checkbox__checkbox {
  position: absolute;
  z-index: -1;
  opacity: 0;
  cursor: pointer;
}

.checkbox__label {
  display: inline-flex;
  align-items: center;
  user-select: none;
  cursor: pointer;
}

.checkbox__label::before {
  content: "";
  display: inline-block;
  width: 1.1em;
  height: 1.1em;
  flex-shrink: 0;
  flex-grow: 0;
  border: 2px solid #aaaaaa;
  transition: 0.5s;
  border-radius: 0.25em;
  margin-right: 0.7em;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: 50% 50%;
}

.checkbox__checkbox:checked + label::before {
  border-color: #0075ff;
  background-color: #0075ff;
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 8 8'%3e%3cpath fill='%23fff' d='M6.564.75l-3.59 3.612-1.538-1.55L0 4.26 2.974 7.25 8 2.193z'/%3e%3c/svg%3e");
}

.checkbox__checkbox:checked + label {
  color: #0075ff;
}

.checkbox__checkbox:not(:disabled):not(:checked) + label:hover::before {
  border-color: #0075ff;
}

.checkbox__checkbox:not(:disabled):active + label::before {
  background-color: #0075ff;
  border-color: #0075ff;
}

.checkbox__checkbox:focus + label::before {
  box-shadow: 0 0 0 0.1rem rgba(0, 123, 255, 0.25);
}

.checkbox__checkbox:focus:not(:checked) + label::before {
  border-color: #0075ff;
}
</style>