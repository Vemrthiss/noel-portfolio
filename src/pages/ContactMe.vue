<template>
    <Layout>
        <div class="contact">
            <div class="contact__heading">
                <h1 class="contact__title">Contact Me</h1>
                <p class="contact__subtitle">Want to drop me a message or want a work commissioned? Fill in the contact form below!</p>
            </div>
            <ContactForm></ContactForm>
        </div>
    </Layout>
</template>

<script>
    import ContactForm from '@/components/ContactForm'

    export default {
        components: {
            ContactForm
        }
    }
</script>

<style lang="scss" scoped>
    .contact {
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;

        &__heading {
            margin: 2rem 0;
        }

        &__title {
            margin: 0;
        }

        &__subtitle {
            margin: 0;
        }
    }
</style>