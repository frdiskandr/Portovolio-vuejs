<template>
	<div class="project-container">
		<section class="dark">
			<div class="container py-4">
				<h1 class="h1 text-center" id="pageHeaderTitle">My Projects</h1>

				<div class="projects" v-for="(project, index) in projects" :key="index">

					<article class="postcard dark blue" v-if="index % 2 == 0">
						<a class="postcard__img_link" href="#">
							<img class="postcard__img" :src="project.image" alt="Image Title" />
						</a>
						<div class="postcard__text">
							<h1 class="postcard__title blue"><a href="#">{{ project.title }}</a></h1>
							<div class="postcard__subtitle small">
								<time datetime="2020-05-25 12:00:00">
									<i class="fas fa-calendar-alt mr-2"></i>{{ project.dateTimes }}
								</time>
							</div>
							<div class="postcard__bar"></div>
							<div class="postcard__preview-txt">{{ project.description }}</div>
							<b class="postcard__tit">Tecnologi: <span v-for="(teknologi, index) in project.teknologies"
									:key="index">{{ `${teknologi}, ` }}</span></b>
							<ul class="postcard__tagbox">
								<li class="tag__item play blue">
									<a :href="project.link" target="_blank" ><i class="fas fa-play mr-2"></i>Demonstrasi</a>
								</li>
								<li class="tag__item green"> <a :href="project.github" target="_blank" ><svg
											xmlns="http://www.w3.org/2000/svg" width="16" height="16"
											fill="currentColor" class="bi bi-github" viewBox="0 0 16 16">
											<path
												d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0 0 16 8c0-4.42-3.58-8-8-8" />
										</svg>Github</a></li>
							</ul>
						</div>
					</article>
					<article class="postcard dark red" v-if="index % 2 != 0">
						<a class="postcard__img_link" href="#">
							<img class="postcard__img" :src="project.image" alt="Image Title" />
						</a>
						<div class="postcard__text">
							<h1 class="postcard__title red"><a href="#">{{ project.title }}</a></h1>
							<div class="postcard__subtitle small">
								<time datetime="2020-05-25 12:00:00">
									<i class="fas fa-calendar-alt mr-2"></i>{{ project.dateTimes }}
								</time>
							</div>
							<div class="postcard__bar"></div>
							<div class="postcard__preview-txt">{{ project.description }}</div>
							<b class="postcard__tit">Tecnologi: <span v-for="(teknologi, index) in project.teknologies"
									:key="index">{{ `${teknologi}, ` }}</span></b>
							<ul class="postcard__tagbox">
								<li class="tag__item play blue">
									<a :href="project.link" target="_blank" ><i class="fas fa-play mr-2"></i>Demonstrasi</a>
								</li>
								<li class="tag__item green"> <a :href="project.github" target="_blank" ><svg
											xmlns="http://www.w3.org/2000/svg" width="16" height="16"
											fill="currentColor" class="bi bi-github" viewBox="0 0 16 16">
											<path
												d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0 0 16 8c0-4.42-3.58-8-8-8" />
										</svg>Github</a></li>
							</ul>
						</div>
					</article>
				</div>
			</div>
		</section>
	</div>
</template>

<script>
import projects from '../datas/projects.json'
export default {
	data() {
		return {
			projects
		}
	}
}
console.log(projects)
console.log(projects.teknologies)
</script>

<style lang="scss" scoped>
/*!
 * Start Bootstrap - Portfolio Bootstrap Theme (http://startbootstrap.com) */
@import url("https://fonts.googleapis.com/css2?family=Baloo+2&display=swap");
$main-green: #79dd09 !default;
$main-green-rgb-015: rgba(121, 221, 9, 0.1) !default;
$main-yellow: #bdbb49 !default;
$main-yellow-rgb-015: rgba(189, 187, 73, 0.1) !default;
$main-red: #bd150b !default;
$main-red-rgb-015: rgba(189, 21, 11, 0.1) !default;
$main-blue: #0076bd !default;
$main-blue-rgb-015: rgba(0, 118, 189, 0.1) !default;

/* This pen */
body {
	font-family: "Baloo 2", cursive;
	font-size: 16px;
	color: #ffffff;
	text-rendering: optimizeLegibility;
	font-weight: initial;
}

.dark {
	background: #110f16;
}


.light {
	background: #f3f5f7;
}

a,
a:hover {
	text-decoration: none;
	transition: color 0.3s ease-in-out;
}

#pageHeaderTitle {
	margin: 2rem 0;
	text-transform: uppercase;
	text-align: center;
	font-size: 2.5rem;
}

/* Cards */
.postcard {
	flex-wrap: wrap;
	display: flex;

	box-shadow: 0 4px 21px -12px rgba(0, 0, 0, 0.66);
	border-radius: 10px;
	margin: 0 0 2rem 0;
	overflow: hidden;
	position: relative;
	color: #ffffff;

	&.dark {
		background-color: #18151f;
	}

	&.light {
		background-color: #e1e5ea;
	}

	.t-dark {
		color: #18151f;
	}

	a {
		color: inherit;
	}

	h1,
	.h1 {
		margin-bottom: 0.5rem;
		font-weight: 500;
		line-height: 1.2;
	}

	.small {
		font-size: 80%;
	}

	.postcard__title {
		font-size: 1.75rem;
	}

	.postcard__img {
		max-height: 180px;
		width: 100%;
		object-fit: cover;
		position: relative;
	}

	.postcard__img_link {
		display: contents;
	}

	.postcard__bar {
		width: 50px;
		height: 10px;
		margin: 10px 0;
		border-radius: 5px;
		background-color: #424242;
		transition: width 0.2s ease;
	}

	.postcard__text {
		padding: 1.5rem;
		position: relative;
		display: flex;
		flex-direction: column;
	}

	.postcard__preview-txt {
		overflow: hidden;
		text-overflow: ellipsis;
		text-align: justify;
		height: 100%;
	}

	.postcard__tagbox {
		display: flex;
		flex-flow: row wrap;
		font-size: 14px;
		margin: 20px 0 0 0;
		padding: 0;
		justify-content: center;

		.tag__item {
			display: inline-block;
			background: rgba(83, 83, 83, 0.4);
			border-radius: 3px;
			padding: 2.5px 10px;
			margin: 0 5px 5px 0;
			cursor: default;
			user-select: none;
			transition: background-color 0.3s;

			&:hover {
				background: rgba(83, 83, 83, 0.8);
			}
		}
	}

	&:before {
		content: "";
		position: absolute;
		top: 0;
		right: 0;
		bottom: 0;
		left: 0;
		background-image: linear-gradient(-70deg, #424242, transparent 50%);
		opacity: 1;
		border-radius: 10px;
	}

	&:hover .postcard__bar {
		width: 100px;
	}
}

@media screen and (min-width: 769px) {
	.postcard {
		flex-wrap: inherit;

		.postcard__title {
			font-size: 2rem;
		}

		.postcard__tagbox {
			justify-content: start;
		}

		.postcard__img {
			max-width: 300px;
			max-height: 100%;
			transition: transform 0.3s ease;
		}

		.postcard__text {
			padding: 3rem;
			width: 100%;
		}

		.media.postcard__text:before {
			content: "";
			position: absolute;
			display: block;
			background: #18151f;
			top: -20%;
			height: 130%;
			width: 55px;
		}

		&:hover .postcard__img {
			transform: scale(1.1);
		}

		&:nth-child(2n+1) {
			flex-direction: row;
		}

		&:nth-child(2n+0) {
			flex-direction: row-reverse;
		}

		&:nth-child(2n+1) .postcard__text::before {
			left: -12px !important;
			transform: rotate(4deg);
		}

		&:nth-child(2n+0) .postcard__text::before {
			right: -12px !important;
			transform: rotate(-4deg);
		}
	}
}

@media screen and (min-width: 1024px) {
	.postcard__text {
		padding: 2rem 3.5rem;
	}

	.postcard__text:before {
		content: "";
		position: absolute;
		display: block;

		top: -20%;
		height: 130%;
		width: 55px;
	}

	.postcard.dark {
		.postcard__text:before {
			background: #18151f;
		}
	}

	.postcard.light {
		.postcard__text:before {
			background: #e1e5ea;
		}
	}
}

/* COLORS */
.postcard .postcard__tagbox .green.play:hover {
	background: $main-green;
	color: black;
}

.green .postcard__title:hover {
	color: $main-green;
}

.green .postcard__bar {
	background-color: $main-green;
}

.green::before {
	background-image: linear-gradient(-30deg,
			$main-green-rgb-015,
			transparent 50%);
}

.green:nth-child(2n)::before {
	background-image: linear-gradient(30deg, $main-green-rgb-015, transparent 50%);
}

.postcard .postcard__tagbox .blue.play:hover {
	background: $main-blue;
}

.blue .postcard__title:hover {
	color: $main-blue;
}

.blue .postcard__bar {
	background-color: $main-blue;
}

.blue::before {
	background-image: linear-gradient(-30deg, $main-blue-rgb-015, transparent 50%);
}

.blue:nth-child(2n)::before {
	background-image: linear-gradient(30deg, $main-blue-rgb-015, transparent 50%);
}

.postcard .postcard__tagbox .red.play:hover {
	background: $main-red;
}

.red .postcard__title:hover {
	color: $main-red;
}

.red .postcard__bar {
	background-color: $main-red;
}

.red::before {
	background-image: linear-gradient(-30deg, $main-red-rgb-015, transparent 50%);
}

.red:nth-child(2n)::before {
	background-image: linear-gradient(30deg, $main-red-rgb-015, transparent 50%);
}

.postcard .postcard__tagbox .yellow.play:hover {
	background: $main-yellow;
	color: black;
}

.yellow .postcard__title:hover {
	color: $main-yellow;
}

.yellow .postcard__bar {
	background-color: $main-yellow;
}

.yellow::before {
	background-image: linear-gradient(-30deg,
			$main-yellow-rgb-015,
			transparent 50%);
}

.yellow:nth-child(2n)::before {
	background-image: linear-gradient(30deg,
			$main-yellow-rgb-015,
			transparent 50%);
}

@media screen and (min-width: 769px) {
	.green::before {
		background-image: linear-gradient(-80deg,
				$main-green-rgb-015,
				transparent 50%);
	}

	.green:nth-child(2n)::before {
		background-image: linear-gradient(80deg,
				$main-green-rgb-015,
				transparent 50%);
	}

	.blue::before {
		background-image: linear-gradient(-80deg,
				$main-blue-rgb-015,
				transparent 50%);
	}

	.blue:nth-child(2n)::before {
		background-image: linear-gradient(80deg, $main-blue-rgb-015, transparent 50%);
	}

	.red::before {
		background-image: linear-gradient(-80deg, $main-red-rgb-015, transparent 50%);
	}

	.red:nth-child(2n)::before {
		background-image: linear-gradient(80deg, $main-red-rgb-015, transparent 50%);
	}

	.yellow::before {
		background-image: linear-gradient(-80deg,
				$main-yellow-rgb-015,
				transparent 50%);
	}

	.yellow:nth-child(2n)::before {
		background-image: linear-gradient(80deg,
				$main-yellow-rgb-015,
				transparent 50%);
	}
}
</style>
