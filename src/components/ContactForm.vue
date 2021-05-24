<template>
    <form action="" class="contact-form">
        <div class="contact-form__name contact-form__row">
            <label for="name" class="contact__name-label contact-form__label">Name</label>
            <input name="name" type="text" class="contact__name-field contact-form__field">
        </div>
        
        <div class="contact-form__email contact-form__row">
            <label for="email" class="contact__email-label contact-form__label">Email</label>
            <input name="email" type="email" class="contact__email-field contact-form__field">
        </div>

        <div class="contact-form__message contact-form__row">
            <label for="message" class="contact__message-label contact-form__label">Message</label>
            <textarea name="message" class="contact__message-field contact-form__field" cols="30" rows="10"></textarea>
        </div>
    </form>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>