<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">

defineProps<{
  href?: string
}>()
</script>
<template>
  <a :href="href">
  <button class="button button--giant">
    <div class="arrow-left"></div>
    <p><slot></slot></p>
    <div class="arrow-right"></div>
  </button>
  </a>
</template>
<style lang="scss">

$smallbeakpoint: 768px;
$mediumbeakpoint: 1024px;
$largebeakpoint: 1200px;

:root {
  --noir: rgb(14, 14, 14);
  --grisFonce: rgb(24,24,24);
  --gris: rgb(40, 40, 40);
  --bleu: rgb(125, 199, 255);
  --primary50: #edeffe ;
  --primary100: #c8cefc ;
  --primary200: #aeb6fb ;
  --primary300: #8895F9 ;
  --primary500: #4e61f6 ;
  --primary700: #3745af ;
  --primary800: #2b3587 ;
  --Grey200: #e5e7ea ;
  --Grey500: #6d717f ;
}

$button--size__giant: 18px;
$button--size__large: 16px;
$button--size__medium: 14px;
$button--size__small: 12px;
$button--size__tiny: 10px;

$button--padding__giant: 16px 24px;
$button--padding__large: 14px 20px;
$button--padding__medium: 12px 16px;
$button--padding__small: 8px 12px;
$button--padding__tiny: 6px 8px;


$button--height__giant: 56px;
$button--height__large: 48px;
$button--height__medium: 40px;
$button--height__small: 32px;
$button--height__tiny: 24px;

$button--borderRadius__default: none;
$button--borderRadius__small: 8px !important;
$button--borderRadius__tiny: 8px !important;

$button--color__default: white;
$button--color__outline: var(--primary500);
$button--color__clear: var(--primary500);
$button--color__disabled: var(--Grey500);


$button--background__default: var(--primary500);
$button--background__default_hover: var(--primary700);
$button--background__default_focus: var(--primary500);
$button--background__default_active: var(--primary800);
$button--background__default_disabled: var(--Grey200);
$button--background__outline: white;
$button--background__outline_hover: var(--primary50);
$button--background__outline_focus: white;
$button--background__outline_active: var(--primary100);
$button--background__outline_disabled: white;
$button--background__clear: white;
$button--background__clear_hover: var(--primary50);
$button--background__clear_focus: white;
$button--background__clear_active: var(--primary100);
$button--background__clear_disabled: white;


$button--rounded__default: 12px;


$button--outline__default: none;
$button--outline__default_focus: 3px solid var(--primary200);
$button--outline__outline: 1.5px solid var(--primary500);
$button--outline__outline_disabled: 1.5px solid var(--Grey500);


$button--outlineOffset__outline: -1.5px;

$button--boxShadow__outline: none;
$button--boxShadow__outline_focus: 0 0 0 3px var(--primary200);
$button--boxShadow__clear: none;
$button--boxShadow__clear_focus: 0 0 0 3px var(--primary200);

$button--arrow__default: url('https://cdn-user-icons.flaticon.com/150979/150979815/1763435416958.svg?token=exp=1763436316~hmac=00561c54a52f24a23167cdb7ee02b59c');
$button--arrow__outline: url('https://cdn-user-icons.flaticon.com/150979/150979815/1763439540456.svg?token=exp=1763440440~hmac=2747fb9f1727aa2d79f115e4854339c7');
$button--arrow__clear: url('https://cdn-user-icons.flaticon.com/150979/150979815/1763439540456.svg?token=exp=1763440440~hmac=2747fb9f1727aa2d79f115e4854339c7');
$button--arrow__disabled: url('https://cdn-user-icons.flaticon.com/150979/150979815/1763437099442.svg?token=exp=1763439337~hmac=ea02bc8b54727c028f56cf17b989f355');

$button--arrowWidth__default: 24px;
$button--arrowHeight__default: 24px;
$button--arrowWidth__tiny: 16px;
$button--arrowHeight__tiny: 16px;

.button {
  color: $button--color__default;
  font-weight: bold;
  border: none;
  background-color: $button--background__default;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: $button--rounded__default;
  cursor: pointer;
  outline: $button--outline__default;

  &:hover {
    background-color: $button--background__default_hover;
    outline: $button--outline__default;
  }

  &:focus {
    background-color: $button--background__default_focus;
    outline: $button--outline__default_focus;
  }

  &:active {
    background-color: $button--background__default_active;
    outline: $button--outline__default;
  }

  & p {
    margin: 0 8px;
  }

  &.button--disabled {
    background-color: $button--background__default_disabled;
    color: $button--color__disabled;
    cursor: not-allowed;
    outline: $button--outline__default;
  }
}
</style>
