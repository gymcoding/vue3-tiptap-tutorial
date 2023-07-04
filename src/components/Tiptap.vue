<template>
	<editor-content :editor="editor" />
</template>

<script setup>
import { useEditor, EditorContent } from '@tiptap/vue-3';
import StarterKit from '@tiptap/starter-kit';

const props = defineProps({
	modelValue: {
		type: String,
		defalt: '',
	},
});

const emit = defineEmits(['update:modelValue']);

const editor = useEditor({
	content: '<p>I’m running Tiptap with Vue.js. 🎉</p>',
	extensions: [StarterKit],
});
</script>
