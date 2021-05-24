<template>
    <a class="social-media-link" :href="link" :class="{'social-media-link--ig': iconObj.icon==='instagram'}">
        <fa-icon class="social-media-link__icon" :icon="[iconObj.iconType, iconObj.icon]"></fa-icon>
    </a>
</template>

<script>
    export default {
        props: {
            iconObj: Object
        },
        computed: {
            link() {
                let link;
                switch (this.iconObj.icon) {
                    case 'github':
                        link = 'https://github.com/Vemrthiss';
                        break
                    case 'instagram':
                        link = 'https://www.instagram.com/ntay_design/'
                        break
                    case 'envelope':
                        link = 'mailto:noeltwc@gmail.com'
                        break
                    default:
                        console.log('Invalid option');
                }
                return link;
            }
        },
        methods: {
            navigate() {

            }
        }
    }
</script>

<style lang="scss" scoped>
    .social-media-link {
        
        &:link, &:visited {
            color: white;
        }

        &__icon {
            width: 3rem;
            height: 3rem;
        }

        &--ig {
            margin-right: 1rem;
        }
    }
</style>