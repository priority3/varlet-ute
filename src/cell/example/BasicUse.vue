<script setup>
import { VarIcon, AppType, dark } from '@varlet/ui'
import { pack, use } from './locale'
import { watchLang, watchDarkMode } from '@varlet/cli/site/utils'

watchLang(use)
watchDarkMode(dark)
</script>

<template>
  <app-type>{{ pack.basicUsage }}</app-type>
  <var-cell> {{ pack.content }} </var-cell>
  <var-cell> {{ pack.content }} </var-cell>

  <app-type>{{ pack.showIcon }}</app-type>
  <var-cell icon="fire" :title="pack.content">
    <template #extra>
      <var-icon name="information" />
    </template>
  </var-cell>
  <var-cell icon="fire" :title="pack.content">
    <template #extra>
      <var-icon name="information" />
    </template>
  </var-cell>

  <app-type>{{ pack.showDesc }}</app-type>
  <var-cell icon="fire" :title="pack.content" :description="pack.description">
    <template #extra>
      <var-icon name="information" />
    </template>
  </var-cell>
  <var-cell :title="pack.content" :description="pack.description" />

  <app-type>{{ pack.showBorder }}</app-type>
  <var-cell border> {{ pack.content }} </var-cell>
  <var-cell border> {{ pack.content }} </var-cell>
</template>
