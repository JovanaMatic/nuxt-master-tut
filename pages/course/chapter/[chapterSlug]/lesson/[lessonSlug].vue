<script setup>
  const courses = useCourse()
  const route = useRoute()
  const chapterSlug = route.params.chapterSlug
  const lessonSlug = route.params.lessonSlug

  const getChapter = computed(() => courses.chapters.find(chapter => chapter.slug === chapterSlug))

  const getLesson = computed(() => getChapter.value.lessons.find(lesson => lesson.slug === lessonSlug))
  console.log(getLesson.value)

</script>

<template>
  <div class="lesson-number">
    <p>Lesson {{ getChapter.number }} - {{ getLesson.number }}</p>
    <h2>{{ getLesson.title }}</h2>
    <div>
      <a v-if="getLesson.sourceUrl"
      :href="getLesson.sourceUrl"
      >
      Download source code
      </a>
      <a v-if="getLesson.downloadUrl"
      :href="getLesson.downloadUrl"
      >
      Download lesson
      </a>
    </div>
  </div>
  <div class="text-section">
    <p>{{ getLesson.text }}</p>
  </div>
</template>

<style scoped>

.lesson-number p {
  text-transform: uppercase;
  color: rgb(157, 156, 156)
}

</style>