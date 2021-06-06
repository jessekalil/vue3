 
<template>
	<div class="home">
		<div class="container">
			<div class="col-content">
				<logo />
				<span class="text-edition">Edição especial | Conteúdo inédito</span>

				<h1 class="title">
					Juntos para
					<br />
					o próximo nível.
				</h1>
				<h2 class="subtitle">
					Um evento para dar o próximo passo na sua
					<br />
					evolução como programadora ou programador.
				</h2>

				<div class="footer-details">
					<div class="detail">
						<calendar-icon />
						<span class="detail-text">
							20 a 27
							<br />
							de junho
						</span>
					</div>
					<div class="detail">
						<video-icon />
						<span class="detail-text">
							Online e
							<br />
							gratuito
						</span>
					</div>
				</div>
			</div>

			<div class="col-form">Form</div>
		</div>
	</div>
</template>

<script lang="ts">
import { defineComponent } from "vue"
import Logo from "@components/Logo.vue"
import CalendarIcon from "@components/CalendarIcon.vue"
import VideoIcon from "@components/VideoIcon.vue"

export default defineComponent({
	components: { Logo, CalendarIcon, VideoIcon },
	setup() {},
})
</script>

<style lang="scss" scoped>
div.home {
	background-image: url("../assets/hero.png");
	height: 100vh;
	display: flex;
	justify-content: center;

	div.container {
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: stretch;

		div.col-content {
			display: flex;
			flex-direction: column;
			justify-content: center;
			color: var(--secondary);

			span.text-edition {
				color: var(--green);
				font-size: 18px;
				font-weight: 500;
				line-height: 16px;
				margin-top: 80px;
			}

			h1.title {
				max-width: 536px;
				font-size: 64px;
				line-height: 64px;
				font-weight: 700;
				margin: 40px 0 16px;
			}

			h2.subtitle {
				font-size: 18px;
				line-height: 28px;
				max-width: 505px;
				font-weight: 400;
			}

			div.footer-details {
				margin-top: 64px;
				display: flex;
				justify-content: space-between;

				div.detail {
					display: flex;
					align-items: center;
					span.detail-text {
						font-size: 24px;
						line-height: 28px;
						margin-left: 32px;
						font-weight: 500;
					}
				}
			}
		}

		div.col-form {
			max-width: 480px;
			width: 100%;
			background: linear-gradient(
				180deg,
				rgba(122, 76, 229, 0.1),
				rgba(4, 211, 97, 0.1)
			);
		}
	}
}

/* xl */
@media (min-width: 1024px) {
	div.home {
		div.container {
			width: 1120px;
		}
	}
}

/* md */
@media (max-width: 1024px) {
	div.home {
		div.container {
			display: flex;
			flex-direction: column;
		}
	}
}
</style>
