<template>
    <section class="wrap-container">
        <div class="intro">
            <div class="intro__description">
                <h1 class="intro__title h1">
                    Двигайся к своей мечте вместе с Соляриком!
                </h1>
                <p class="intro__text p1">Непрерывная система мотивации школьников к учебе, спорту труду и творчеству.
                    Регестрируйся и получи первые Солярики</p>
            </div>
            <div class="intro__form-container">
                <form action="" class="intro__form">
                    <input type="text" class="intro__input p2" placeholder="Логин">
                    <input type="text" class="intro__input p2" placeholder="Пароль">
                    <button class="btn">Воити в кабинет</button>
                    <button class="btn-text">Забыли пароль?</button>
                </form>
            </div>
        </div>
    </section>
</template>

<script setup>

</script>

<style>
.wrap-container {
    width: 100%;
    background: var(--dark)
}

.intro {
    max-width: 1440px;
    margin: 0 auto;
    padding: 0 60px;
    display: flex;
    justify-content: space-between;
    min-height: 668px;
    box-sizing: border-box
}

.intro__description {
    padding-top: 80px;
    max-width: 660px;
}

.intro__title {
    color: var(--white);
}

.intro__text {
    margin-top: 90px;
    color: var(--white);
    max-width: 517px;
}


.intro__form-container {
    padding-top: 220px;
}

.intro__form {
    padding: 24px;
    background: var(--dark);
    display: flex;
    flex-direction: column;
    gap: 24px;
    align-items: center;
}

.intro__input {
    padding: 16px;
    border: 2px solid var(--roseBege);
    background: var(--white);
    color: var(--roseBege)
}

.intro__input::placeholder {
    color: var(--roseBege)
}

.intro__input:hover {
    background: var(--lightBege);
}

.intro__input:focus {
    background: var(--white);
    color: var(--dark)
}

.intro__input:active,
.intro__input:focus {
    outline: none;
}

.intro__input:first-child {
    margin-top: 32px;
    margin-bottom: 8px;
}



</style>