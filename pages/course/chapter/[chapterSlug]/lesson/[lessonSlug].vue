<script setup>
  const courses = useCourse()
  const route = useRoute()
  const chapterSlug = route.params.chapterSlug
  const lessonSlug = route.params.lessonSlug

  const getChapter = courses.chapters.find(chapter => chapter.slug === chapterSlug)

  const getLesson = getChapter.lessons.find(lesson => lesson.slug === lessonSlug)

</script>

<template>
  <div>
    <h4>Lesson</h4>
    <p>This is lesson</p>
  </div>
</template>

<style scoped>

</style>