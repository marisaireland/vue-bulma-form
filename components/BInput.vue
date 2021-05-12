<template>
  <div>
    <label
      :for="_uid"
      class="label"
    >
      <slot name="label" />
    </label>
    <div class="control">
      <input
        :id="_uid"
        class="input"
        type="text"
        :value="value"
        @input="$emit('input', $event.target.value)"
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'BInput',
  props: {
    value: {
      type: String,
      default: '',
    },
  },
};
</script>
