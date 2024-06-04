<script setup>
  const courses = useCourse()
  const route = useRoute()
  const chapterSlug = route.params.chapterSlug
  const lessonSlug = route.params.lessonSlug

  const getChapter = computed(() => courses.chapters.find(chapter => chapter.slug === chapterSlug))

  const getLesson = computed(() => getChapter.value.lessons.find(lesson => lesson.slug === lessonSlug))

</script>

<template>
  <div>
    <h4>Lesson</h4>
    <p>{{ getLesson.title }}</p>
    <p>{{ getLesson.text }}</p>
  </div>
</template>

<style scoped>

</style>