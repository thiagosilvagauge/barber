<template>
    <ion-content class="background-image" no-scroll padding>
        <div class="content">
            <ion-img :src="barberLogo" alt="teste"></ion-img>
            <form class="form">
                <ion-item>
                    <ion-input type="text" placeholder="Telefone" required></ion-input>
                </ion-item>
                <ion-item>
                    <ion-input type="password" placeholder="Senha" required></ion-input>
                </ion-item>
                <ion-button :router-link="{ path: '/home' }" expand="full">Entrar</ion-button>
            </form>
        </div>
    </ion-content>
</template>

<script>
import { IonContent, IonImg, IonItem, IonInput, IonButton } from '@ionic/vue';
export default {
    name: 'Login',
    components: {
        IonContent,
        IonImg,
        IonItem,
        IonInput,
        IonButton
    },
    data () {
        return {
            barberLogo: 'assets/barberlogo.png'
        }
    }
}
</script>

<style>
    .background-image {
        --background: url('../../public/assets/login/bg.png') no-repeat top right / 100%;
    }
    .content {
        background: linear-gradient(to top, rgb(0 0 0 / 1) 40%, rgba(0 0 0 / 0.3) 100%);
        width: 100%;
        height: 100%;
        box-sizing: border-box;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        gap: 1rem
    }

    ion-img {
        position: relative;
        width: 250px;
    }

    ion-item {
        margin-top: 1rem;
        --background: var(--ion-color-transparent);
        border: 1px solid var(--ion-color-primary-contrast);
    }

    ion-input {
        --color: var(--ion-color-primary-contrast) !important;
        border-color: none;
    }

    ion-button {
        margin-top: 1rem;
    }

</style>