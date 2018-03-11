<template lang="pug">
	.wrapper.main-page
		header.main-header
			section.about
				.about-img
					img(src="../assets/images/content/Ira-Noschenko.jpg", class="about-img-src", alt="Ира Нощенко")
				h1.about-ttl Ира Нощенко
				h2.about-subttl Личный сайт веб разработчика
				ul.social-wrap
					li.social-item
						a.social-link.vk-ico вКонтакте
					li.social-item
						a.social-link.gt-ico Github
					li.social-item
						a.social-link.ln-ico Linkedin
			nav.main-nav
				ul.nav-wrap
					li.nav-item
						router-link(to='/works', class="nav-link") Мои работы
					li.nav-item
						router-link(to='/about', class="nav-link") Обо мне
					li.nav-item
						router-link(to='/blog', class="nav-link") Блог
</template>

<script>
    export default {
        name: 'HomePage',
        data () {
            return {
                msg: 'Welcome to Your Vue.js App'
            }
        }
    }
</script>

<style lang="scss">
	
	$green-light: #649257;
	$green-dark: #487f39;
	
	.wrapper.main-page {
		background: url("../assets/images/bg/water.jpg") 50% 50% no-repeat;
	}
	.main-header {
		position: absolute;
		top: 0;
		right: 0;
		bottom: 0;
		left: 0;
		width: 380px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		height: 395px;
		margin: auto;
		background: rgba(43, 65, 44, .6);
		color: #fff;
		border-radius: 5px;
		
	}
	
	.about { padding: 40px;
		&-img { position: relative; display: block; width: 141px; height: 141px; margin: auto; border-radius: 50%; overflow: hidden; background: #ccc;
			&-src {position: absolute; top: 0; left: 0; right: 0; width: 100%; margin: auto; display: block; }
		}
		
		&-ttl { font-size: 28px; font-weight: 500; }
		&-subttl {font-size: 16px; }
	}
	
	.social {
		&-wrap { display: flex; width: 100%; height: 22px; }
		&-item { width: calc(100% / 3); text-indent: -9999px; }
		&-link { width: 100%; height: 100%; display: block; }
	}
	
	.main-nav { width: 100%; }
	
	.nav {
		&-wrap { display: flex; justify-content: space-around; width: 100%; height: 45px; align-items: center; padding-left: 0;}
		&-item { width: calc(100% / 3); height: 100%; background: $green-light; border-right: 2px solid rgba(255, 255, 255, .6); cursor: pointer; transition: background .8s;
			&:first-child { border-bottom-left-radius: 5px;}
			&:last-child {  border-bottom-right-radius: 5px; border-right: none; }
			&:hover {background: $green-dark;}
		}
		&-link { display: flex; justify-content: center; align-items: center;  width: 100%; height: 100%; color: #fff; text-decoration: none;}
	}


</style>
