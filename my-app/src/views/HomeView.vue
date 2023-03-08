
<script setup lang="ts">
import { ref } from 'vue';
import Button from '@gits-id/button';
import VAppBar from '@gits-id/app-bar';

const isOpen = ref(true);
</script>
import type { VBtn } from '@gits-id/button';


import VAlert from '@gits-id/alert';


import type VAlert from '@gits-id/alert';

<style>
.app-bar-indigo {
  --app-bar-bg-color: theme('colors.indigo.500');
  --app-bar-color: theme('colors.white');
}
</style>

<template>
  <VAppBar bordered> Helo word <br> <br> Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem
    Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type
    and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into
    electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset
    sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker
    including versions of Lorem Ipsum.</VAppBar>
  <Button @click="isOpen = !isOpen">Toggle Alert</Button>
  <VAlert v-model="isOpen" color="primary" class="mt-4" solid dismissable>
    Alert text
  </VAlert>
  <div class="container mx-auto p-6 space-y-3">
    <h1 class="text-3xl font-bold text-gray-800">GITS UI</h1>

    <VAlert color="error"> Alert text </VAlert>
    <VAlert> Alert text </VAlert>
    <VAlert color="primary"> Alert text </VAlert>
    <VAlert color="secondary"> Alert text </VAlert>
    <VAlert color="info"> Alert text </VAlert>
    <VAlert color="warning"> Alert text </VAlert>
    <VAlert color="success"> Alert text </VAlert>
    <VAlert color="error"> Alert text </VAlert>
    <VAlert color="dark"> Alert text </VAlert>
    <br><br>
    <VAlert solid> default </VAlert>
    <VAlert solid color="primary"> primary </VAlert>
    <VAlert solid color="secondary"> secondary </VAlert>
    <VAlert solid color="info"> info </VAlert>
    <VAlert solid color="warning"> warning </VAlert>
    <VAlert solid color="success"> success </VAlert>
    <VAlert solid color="error"> error </VAlert>
    <VAlert solid color="dark"> dark </VAlert>
    <br><br>
    <VAlert outlined> default </VAlert>
    <VAlert outlined color="primary"> primary </VAlert>
    <VAlert outlined color="secondary"> secondary </VAlert>
    <VAlert outlined color="info"> info </VAlert>
    <VAlert outlined color="warning"> warning </VAlert>
    <VAlert outlined color="success"> success </VAlert>
    <VAlert outlined color="error"> error </VAlert>
    <VAlert outlined color="dark"> dark </VAlert>
    <br><br>
    <VAppBar shadow> Hello World </VAppBar>
    <VAppBar size="auto" shadow="sm"> Hello World </VAppBar>
    <VAppBar shadow="md"> Hello World </VAppBar>
    <VAppBar shadow="lg"> Hello World </VAppBar>
    <VAppBar shadow="xl"> Hello World </VAppBar>
    <VAppBar shadow="2xl"> Hello World </VAppBar>
    <VAppBar shadow="inner"> Hello World </VAppBar>
    <VAppBar shadow="none"> Hello World </VAppBar>

    <VBtn color="primary"> Click me </VBtn>
    <VAutocomplete clearable />
    <VInput placeholder="Type something..." />

    <br><br><br><br>
    <VAvatar name="John Doe" :max-initial="1" />
    <VAvatar color="primary" src="path-to-image.png" />
    <VAvatar src="path-to-image.jpg" alt="John Doe" />
    <VAvatar shape="square" src="path-to-image.jpg" alt="John Doe" />
    <VAvatar shape="rounded" src="path-to-image.jpg" alt="John Doe" />
    <VBadge> Hello World </VBadge>
    <br><br><br>



    <VBtn @click="isOpen = !isOpen">Open BottomSheet</VBtn>
    <VBottomSheet v-model="isOpen">
      <VBottomSheetBody>
        A quick brown fox leaps over the lazy dog.
      </VBottomSheetBody>
    </VBottomSheet>
    <br><br><br>

    <VBtn @click="isOpen = !isOpen">Open BottomSheet</VBtn>
  <VBottomSheet v-model="isOpen">
    <VBottomSheetHeader> Sheet Title </VBottomSheetHeader>
    <VBottomSheetBody>
      A quick brown fox leaps over the lazy dog.
    </VBottomSheetBody>
  </VBottomSheet>
  <br><br>
  <VCard> Hello World </VCard>
  <br><br>
  <VCollapsible
    
    header-class=""
    active-class="font-semibold text-red-500 bg-red-200 rounded-t-lg"
    inactive-class="text-red-500 bg-red-50"
    wrapper-class="rounded-lg"
    activator-class="hover:bg-red-200 hover:text-red-500"
    panel-class="border p-4 rounded-b-lg"
  />
  </div>
</template>

