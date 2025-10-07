<script setup lang="ts">
    const { navigateTo } = usePageTransition();
</script>

<template>
    <ContentLayout>
        <div class="flex flex-col gap-4 items-center py-4">
            <h1 class="text-5xl font-bold">Portfolio Page</h1>
            <cardLayout>
                <Card title="Project 1" description="Description of Project 1" miniature="images/testPic1.jpeg" picLoc="right" articleID="1" :navigateTo="navigateTo"/>
                <Card title="Project 2" description="Description of Project 2" miniature="images/testPic2.webp" picLoc="left" articleID="2" :navigateTo="navigateTo"/>
                <Card title="Project 3" description="Description of Project 3" miniature="images/testPic3.jpeg" picLoc="right" articleID="3" :navigateTo="navigateTo"/>
                <Card title="Project 4" description="Description of Project 4" miniature="images/herobg.jpg" articleID="4" :navigateTo="navigateTo"/>
            </cardLayout>
        </div>
    </ContentLayout>
</template>
