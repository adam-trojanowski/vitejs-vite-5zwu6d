<template>
  <footer
    class="w-full p-4 bg-white border-t border-gray-200 shadow md:flex md:items-center md:justify-between md:p-6 dark:bg-gray-800 dark:border-gray-600"
  >
    <a
      href="https://thegoodcode.io/"
      class="flex items-center"
    >
      <img
        src="https://www.thegoodcode.io/static/8c8a1d90d4a3a2f290af76a174872bbb/dba53/logo.webp"
        class="h-8 mr-3"
        alt="TheGoodCode Logo"
      />
    </a>
    <div class="flex justify-center items-center">
      <p
        :class="{
          'cursor-not-allowed opacity-50': props.page === 0,
          'cursor-pointer': props.page !== 0,
        }"
        @click="$emit('pageChange', Math.max(props.page - 1, 0))"
        class="cursor-pointer inline-flex items-center px-4 py-2 mr-3 text-sm font-medium text-gray-500 bg-white border border-gray-300 rounded-lg hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
      >
        <svg
          aria-hidden="true"
          class="w-5 h-5 mr-2"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M7.707 14.707a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 1.414L5.414 9H17a1 1 0 110 2H5.414l2.293 2.293a1 1 0 010 1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
        Previous
      </p>
      <p
        @click="
          $emit('pageChange', Math.min(props.page + 1, props.pageCount - 1))
        "
        :class="{
          'cursor-not-allowed opacity-50': props.page === props.pageCount - 1,
          'cursor-pointer': props.page !== props.pageCount - 1,
        }"
        class="cursor-pointer inline-flex items-center px-4 py-2 text-sm font-medium text-gray-500 bg-white border border-gray-300 rounded-lg hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
      >
        Next
        <svg
          aria-hidden="true"
          class="w-5 h-5 ml-2"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </p>
    </div>
    <ul
      class="flex flex-wrap items-center mt-3 text-sm font-medium text-gray-500 dark:text-gray-400 sm:mt-0"
    >
      <li>
        <a
          href="#"
          class="mr-4 hover:underline md:mr-6"
        >
          Front-end Vue3 Assessment
        </a>
      </li>
    </ul>
  </footer>
</template>

<script lang="ts" setup>
  const props = withDefaults(
    defineProps<{ page: number; pageCount: number }>(),
    { page: 1 }
  )

  defineEmits({
    pageChange: (value: number) => value,
  })
</script>
