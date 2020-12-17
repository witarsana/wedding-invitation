<template>
	<div id="app" class="overflow-x-hidden relative"> 
		<div class="wa-place fixed w-16 h-16 bg-white rounded-full z-40 flex shadow ">

			<a  href="#" class="text-red-500 block m-auto">
				<svg class="fill-current m-auto social-icon" width="40" height="40" viewBox="0 0 16 16"><g ><path  d="M13.641 2.325A7.869 7.869 0 0 0 8.032 0C3.663 0 .107 3.556.107 7.928c0 1.397.366 2.763 1.059 3.963L.041 16l4.203-1.103a7.929 7.929 0 0 0 3.787.966h.003c4.369 0 7.928-3.556 7.928-7.928a7.887 7.887 0 0 0-2.322-5.609zm-5.607 12.2a6.583 6.583 0 0 1-3.356-.919l-.241-.144-2.494.653.666-2.431-.156-.25a6.537 6.537 0 0 1-1.009-3.506 6.599 6.599 0 0 1 6.594-6.591c1.759 0 3.416.688 4.659 1.931a6.554 6.554 0 0 1 1.928 4.662c-.003 3.637-2.959 6.594-6.591 6.594zm3.613-4.937c-.197-.1-1.172-.578-1.353-.644s-.313-.1-.447.1c-.131.197-.512.644-.628.778-.116.131-.231.15-.428.05s-.838-.309-1.594-.984c-.588-.525-.987-1.175-1.103-1.372s-.013-.306.088-.403c.091-.088.197-.231.297-.347s.131-.197.197-.331c.066-.131.034-.247-.016-.347s-.447-1.075-.609-1.472c-.159-.388-.325-.334-.447-.341-.116-.006-.247-.006-.378-.006s-.347.05-.528.247c-.181.197-.694.678-.694 1.653s.709 1.916.809 2.05c.1.131 1.397 2.134 3.384 2.991.472.203.841.325 1.128.419.475.15.906.128 1.247.078.381-.056 1.172-.478 1.338-.941s.166-.859.116-.941c-.047-.088-.178-.137-.378-.238z"></path></g></svg>
			</a>
		</div>
		<nav :class="openBar==true? 'open':''" class="nav flex xl:hidden md:hidden fixed">
            <ul class="menu-nav font-light text-gray-400 text-2xl w-screen flex flex-col justify-around   h-screen bg-gray-800">
                <li :class="section=='home'? 'focus':''" class="mt-20 menu-link w-full text-center">
                    <a @click="toogleMenu()" href="#home" class="menu-nav-link">HOME</a>
                </li>
                <li :class="section=='about'? 'focus':''" class="menu-link w-full text-center">
                    <a @click="toogleMenu()" href="#about" class="menu-nav-link">TENTANG KAMI</a>
                </li>
                <li :class="section=='feature'? 'focus':''" class="menu-link w-full text-center">
                    <a @click="toogleMenu()" href="#feature" class="menu-nav-link">FITUR</a>
                </li>
                <li :class="section=='price'? 'focus':''" class="menu-link w-full text-center">
                    <a @click="toogleMenu()" href="#price" class="menu-nav-link">HARGA</a>
                </li>
				<li :class="section=='theme'? 'focus':''" class="menu-link w-full text-center">
                    <a @click="toogleMenu()" href="#theme" class="menu-nav-link">TEMA</a>
                </li>
				<li :class="section=='contact'? 'focus':''" class="menu-link w-full text-center">
                    <a @click="toogleMenu()" href="#contact" class="menu-nav-link">KONTAK</a>
                </li>
            </ul>
        </nav>
		<nav :class="scroll>40? 'active':''" class="flex text-gray-700 justify-between h-16 px-5 md:px-10 xl:px-12 items-center w-full fixed z-40">
			<a href="#" class="logo text-xl md:text-2xl xl:text-4xl font-light flex justify-between items-center">
				<img src="./assets/img/logo.png" class="h-10 logos" alt="" srcset="">
				<span class="block ml-2 md:ml-3 xl:ml-5 text">INMOTIOON</span>
			</a>
			<ul class=" text-sm font-semibold tracking-wider hidden md:flex xl:flex">
				<li class="mr-4"><a :class="section=='home'? 'focus':''" class="hover:text-red-500" href="#home">HOME</a></li>
				<li class="mr-4"><a :class="section=='about'? 'focus':''" class="hover:text-red-500" href="#about">TENTANG KAMI</a></li>
				<li class="mr-4"><a :class="section=='feature'? 'focus':''" class="hover:text-red-500" href="#feature">FITUR</a></li>
				<li class="mr-4"><a :class="section=='price'? 'focus':''" class="hover:text-red-500" href="#price">HARGA</a></li>
				<li class="mr-4"><a :class="section=='theme'? 'focus':''" class="hover:text-red-500" href="#theme">TEMA</a></li>
				<li class="mr-4"><a :class="section=='contact'? 'focus':''" class="hover:text-red-500" href="#contact">KONTAK</a></li>
			</ul>
			<div @click="toogleMenu()" class="flex relative md:hidden xl:hidden burger_container h-full w-12" href="">
				<div :class="scroll>40? 'active':''"  class="menu-btn m-auto">
					<span :class="openBar==true? 'open':''" class="menu-btn__burger">

					</span>
            	</div>
			</div>
		</nav>
		<section id="home" class="min-h-screen flex flex-col home">
			<div class="pad w-full h-16"></div>
			<div class="content flex-1 flex justify-end relative">
				<div class="absolute flex md:flex xl:hidden w-full h-full bg-white cover opacity-85"></div>
				<div class="content-home my-auto flex relative">
					
					<div class="content-left flex-1 none md:none xl:flex"></div>
					<div class="content-right sm:w-screen md:w-screen xl:w-auto px-10 relative md:ml-5 xl:ml-0  md:mr-18 xl:mr-30">
						
						<h1 :class="section=='home'? 'fade-bot':''" class="title-home text-4xl mb-5 md:mb-10 xl:mb-16 text-red-500 ">Undangan Digital Bali</h1>
						<p :class="section=='home'? 'fade-left':''" class="text-xl mb-5 text-gray-900 md:text-gray-900 xl:text-gray-700 tracking-wide ">Undangan digital keren untuk acara spesial <b>Kamu</b></p>
						<p :class="section=='home'? 'fade-left':''" class="text-xl font-light text-gray-900 md:text-gray-900 xl:text-gray-700 tracking-wide ">Buat dan sebarkan undangan digital untuk acara <br> 
						spesial kamu dalam satu langkah mudah yang <br>
						tentunya <span class="uppercase font-bold text-base text-red-500">cepat, murah, efisien</span></p>
						<ul  class="flex mt-10  md:mt-15 xl:mt-20 mb-10">
							<li :class="section=='home'? 'fadein':''"><a class="px-3 md:px-6 xl:px-6 text-white text-xs md:text-sm xl:text-sm hover:opacity-75 font-semibold py-3 rounded-full bg-red-500" href="#">Tanya Admin</a></li>
							<li :class="section=='home'? 'fadein':''"><a class="ml-5 px-3 md:px-6 xl:px-6 text-white text-xs md:text-sm xl:text-sm hover:opacity-75 font-semibold py-3 rounded-full border border-red-500 text-red-500" href="#testimoni">Lihat Testimoni</a></li>
						</ul>
					</div>
					
				</div>
			</div>
		</section>
		<section id="about" class="min-h-screen flex flex-col about">
			<div class="pad w-full h-16 bg-white"></div>
			<div class="content flex-1 bg-white flex flex-col ">
				<div class="content-title flex justify-between mt-0 md:mt-10 xl:mt-10 px-12">
					<div class="title-text text-red-500 text-4xl">Tentang Kami</div>
					<div class="title-line ml-10 flex-1 border-b  border-red-300"></div>
				</div>
				<div class="content-fill mt-10 tracking-wider text-gray-700 text-base px-12 text-center">
					Inmotioon adalah situs penyedia layanan undangan digital atau undangan online yang berbasis website sehingga mudah digunakan dan dibagikan ke tamu undanganmu. Tidak perlu lagi cetak banyak kartu undangan dan mahal-mahal, kini kamu dapat membagikan undangan hanya dengan membagikan satu link atau alamat webstite yang gampang untuk diingat dan disebarkan. Inmotioon berlokasi di Badung, Bali, dengan harga murah dan banyak fitur menarik seperti Buku Tamu, Maps (petunjuk arah), Backsound (musik latar), Custom Domain dll, mejadikan undangan pernikahan kamu lebih spesial, keren dan unik.
				</div>
				<div  class="about-card flex flex-col px-5 md:px-12 xl:px-12 md:flex-col xl:flex-row justify-between items-center mt-8 md:mt-8 xl:mt-16">
					<div  class="cards w-full md:w-full xl:w-1/3 px-0 md:px-3 xl:px-6 mb-8 md:mb-0 xl:mb-0">
						<div :class="section=='about'? 'fadein':''" class="card-wrap border-t border-gray-100 px-2 py-2 w-full h-64 md:h-48 xl:h-48 shadow-2xl rounded-lg flex justify-between items-center">
							<div class="card-left flex-1 text-red-500 ml-2">
								<svg class="fill-current w-10 md:w-12 xl:w-16"  viewBox="0 0 64 64"><g fill=""><path d="M28.977,27.141c1.886,0.368,3.687,1.28,5.145,2.738c3.899,3.899,3.899,10.243,0,14.142 l-7.071,7.071c-3.899,3.899-10.243,3.899-14.142,0s-3.899-10.243,0-14.142l7.071-7.071c0.349-0.349,0.724-0.656,1.11-0.943 c-0.185-1.56-0.154-3.141,0.119-4.691c-1.468,0.673-2.849,1.598-4.057,2.805l-7.071,7.071c-5.459,5.459-5.459,14.34,0,19.799 s14.34,5.459,19.799,0l7.071-7.071c5.459-5.459,5.459-14.34,0-19.799c-1.998-1.998-4.456-3.257-7.036-3.792 C29.265,24.466,28.96,25.803,28.977,27.141z"></path> <path  d="M34.121,10.08l-7.071,7.071c-5.459,5.459-5.459,14.34,0,19.799c1.997,1.997,4.455,3.256,7.033,3.792 c0.648-1.207,0.968-2.543,0.952-3.879c-1.891-0.366-3.696-1.279-5.157-2.741c-3.899-3.899-3.899-10.243,0-14.142l7.071-7.071 c3.899-3.899,10.243-3.899,14.142,0s3.899,10.243,0,14.142l-7.071,7.071c-0.348,0.348-0.722,0.654-1.106,0.941 c0.187,1.564,0.135,3.148-0.138,4.7c1.474-0.674,2.86-1.601,4.072-2.813l7.071-7.071c5.459-5.459,5.459-14.34,0-19.799 S39.58,4.621,34.121,10.08z"></path></g></svg>
							</div>
							<div class="card-right ml-8 pr-3">
								<h1 class="border-b text-3xl  md:text-xl xl:text-3xl text-red-500 border-gray-300">Online</h1>
								<p class=" text-base md:text-base xl:text-sm  mt-3 text-gray-800">Berbagi undangan kamu menjadi lebih mudah karena undanganmu tersedia secara online</p>
							</div>
						</div>
					</div>
					<div  class="cards w-full md:w-full xl:w-1/3 px-0 md:px-3 xl:px-6 mb-8 md:mb-0 xl:mb-0">
						<div :class="section=='about'? 'fade-bot':''" class="card-wrap border-t border-gray-100 px-2 py-2 w-full h-64 md:h-48 xl:h-48 shadow-2xl rounded-lg flex justify-between items-center">
							<div class="card-left flex-1 text-red-500 ml-2">
								<svg class="fill-current  w-10 md:w-12 xl:w-16"  viewBox="0 0 438.533 438.533"><g ><path d="M409.133 109.203c-19.608-33.592-46.205-60.189-79.798-79.796C295.736 9.801 259.058 0 219.273 0c-39.781 0-76.47 9.801-110.063 29.407-33.595 19.604-60.192 46.201-79.8 79.796C9.801 142.8 0 179.489 0 219.267c0 39.78 9.804 76.463 29.407 110.062 19.607 33.592 46.204 60.189 79.799 79.798 33.597 19.605 70.283 29.407 110.063 29.407s76.47-9.802 110.065-29.407c33.593-19.602 60.189-46.206 79.795-79.798 19.603-33.596 29.403-70.284 29.403-110.062.001-39.782-9.8-76.472-29.399-110.064zm-55.391 188.005c-13.894 23.791-32.736 42.64-56.527 56.534-23.791 13.894-49.771 20.834-77.945 20.834-28.167 0-54.149-6.94-77.943-20.834-23.791-13.895-42.633-32.743-56.527-56.534-13.897-23.791-20.843-49.772-20.843-77.941 0-28.171 6.949-54.152 20.843-77.943 13.891-23.791 32.738-42.637 56.527-56.53 23.791-13.895 49.772-20.84 77.943-20.84 28.173 0 54.154 6.945 77.945 20.84 23.791 13.894 42.634 32.739 56.527 56.53 13.895 23.791 20.838 49.772 20.838 77.943 0 28.169-6.943 54.15-20.838 77.941z"></path><path d="M246.68 109.631h-18.274c-2.669 0-4.853.859-6.57 2.57-1.706 1.713-2.565 3.9-2.565 6.565v100.5h-63.953c-2.667 0-4.853.855-6.567 2.564-1.712 1.712-2.568 3.901-2.568 6.571v18.271c0 2.666.856 4.856 2.568 6.567 1.715 1.711 3.905 2.566 6.567 2.566h91.367c2.662 0 4.853-.855 6.561-2.566 1.711-1.711 2.573-3.901 2.573-6.567V118.766c0-2.663-.862-4.849-2.573-6.565-1.71-1.711-3.9-2.57-6.566-2.57z"></path></g></svg>
							</div>
							<div class="card-right ml-8 pr-3">
								<h1 class="border-b text-3xl  md:text-xl xl:text-3xl text-red-500 border-gray-300">Proses Cepat</h1>
								<p class="text-base md:text-base xl:text-sm mt-3 text-gray-800">Dalam waktu 1 hari Kamu sudah bisa mendapatkan undangan digitalmu sendiri</p>
							</div>
						</div>
					</div>
					<div  class="cards w-full md:w-full xl:w-1/3 px-0 md:px-3 xl:px-6 mb-8 md:mb-0 xl:mb-0">
						<div :class="section=='about'? 'fadein':''" class="card-wrap border-t border-gray-100 px-2 py-2 w-full h-64 md:h-48 xl:h-48 shadow-2xl rounded-lg flex justify-between items-center">
							<div class="card-left flex-1 text-red-500 ml-2">
								<svg class="fill-current w-10 md:w-12 xl:w-16"  viewBox="0 0 48 48">
									<g >
										<path d="M38 22H22v11.99h16V22zm8 16V9.96C46 7.76 44.2 6 42 6H6C3.8 6 2 7.76 2 9.96V38c0 2.2 1.8 4 4 4h36c2.2 0 4-1.8 4-4zm-4 .04H6V9.94h36v28.1z"></path>
									</g>
								</svg>
							</div>
							<div class="card-right ml-8 pr-3">
								<h1 class="border-b  text-3xl  md:text-xl xl:text-3xl text-red-500 border-gray-300">Menarik</h1>
								<p class="text-base md:text-base xl:text-sm mt-3 text-gray-800">Desain tema responsive sehingga nyaman digunakan di smartphone atau PC</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</section>
		<section id="feature" class="min-h-screen flex flex-col feature">
			<div class="pad w-full h-16 "></div>
			<div class="content flex flex-col px-12">
				<div class="content-title flex justify-between mt-0 md:mt-10 xl:mt-10">
					<div class="title-text text-red-500 text-4xl">Fitur Undangan</div>
					<div class="title-line ml-10 flex-1 border-b  border-red-300"></div>
				</div>
			</div>
			<div  class="content-red px-2 py-10 flex-1 mt-12 bg-red-300 flex flex-col ">
				<div :class="section=='feature'? 'fade-lefts':''" class="feature-top py-4 px-4 flex flex-col md:flex-col xl:flex-row">
					<div class="feature-content w-full md:w-full xl:w-1/3 mb-4 md:mb-4 xl:mb-0 px-2 flex text-white">
						<div class="icon ">
							<svg class="fill-current"  width="30" height="30" viewBox="0 0 64 64"><g ><path  d="M50,1H14c-2.209,0-4,1.791-4,4v55c0,0.356,0.189,0.686,0.498,0.865c0.308,0.179,0.688,0.181,0.998,0.003 L32,49.152l20.504,11.716C52.657,60.956,52.829,61,53,61c0.174,0,0.347-0.045,0.502-0.135C53.811,60.686,54,60.356,54,60V5 C54,2.791,52.209,1,50,1z"></path></g></svg>
						</div>
						<div class="icon flex-1 ml-2">
							<h3>Informasi Acara</h3>
							<p>Informasi mengenai detail acara kamu, mulai dari waktu, lokasi dan lain-lain.</p>
						</div>
					</div>
					<div class="feature-content w-full md:w-full xl:w-1/3 mb-4 md:mb-4 xl:mb-0 px-2 flex text-white">
						<div class="icon ">
							<svg class="fill-current"  width="30" height="30" viewBox="0 0 64 64"><g ><path  d="M50,1H14c-2.209,0-4,1.791-4,4v55c0,0.356,0.189,0.686,0.498,0.865c0.308,0.179,0.688,0.181,0.998,0.003 L32,49.152l20.504,11.716C52.657,60.956,52.829,61,53,61c0.174,0,0.347-0.045,0.502-0.135C53.811,60.686,54,60.356,54,60V5 C54,2.791,52.209,1,50,1z"></path></g></svg>
						</div>
						<div class="icon flex-1 ml-2">
							<h3>Google Maps</h3>
							<p>Terintegrasi dengan google maps, memudahkan untuk menemukan lokasi acara.</p>
						</div>
					</div>
					<div class="feature-content w-full md:w-full xl:w-1/3 mb-0 md:mb-0 xl:mb-0 px-2 flex text-white">
						<div class="icon ">
							<svg class="fill-current"  width="30" height="30" viewBox="0 0 64 64"><g ><path  d="M50,1H14c-2.209,0-4,1.791-4,4v55c0,0.356,0.189,0.686,0.498,0.865c0.308,0.179,0.688,0.181,0.998,0.003 L32,49.152l20.504,11.716C52.657,60.956,52.829,61,53,61c0.174,0,0.347-0.045,0.502-0.135C53.811,60.686,54,60.356,54,60V5 C54,2.791,52.209,1,50,1z"></path></g></svg>
						</div>
						<div class="icon flex-1 ml-2">
							<h3>Gallery</h3>
							<p>Tempat untuk menampilkan foto-foto atau video terbaik kamu.</p>
						</div>
					</div>
				</div>
				<div :class="section=='feature'? 'fade-right':''" class="feature-bottom py-4 px-4 flex flex-col md:flex-col xl:flex-row">
					<div class="feature-content w-full md:w-full xl:w-1/3 mb-4 md:mb-4 xl:mb-0 px-2 px-2 flex text-white">
						<div class="icon ">
							<svg class="fill-current"  width="30" height="30" viewBox="0 0 64 64"><g ><path  d="M50,1H14c-2.209,0-4,1.791-4,4v55c0,0.356,0.189,0.686,0.498,0.865c0.308,0.179,0.688,0.181,0.998,0.003 L32,49.152l20.504,11.716C52.657,60.956,52.829,61,53,61c0.174,0,0.347-0.045,0.502-0.135C53.811,60.686,54,60.356,54,60V5 C54,2.791,52.209,1,50,1z"></path></g></svg>
						</div>
						<div class="icon flex-1 ml-2">
							<h3>Buku Tamu</h3>
							<p>Tamu Undangan dapat memberikan ucapan dan kamu dapat mengetahui jumlah tamu yang akan hadir</p>
						</div>
					</div>
					<div class="feature-content w-full md:w-full xl:w-1/3 mb-4 md:mb-4 xl:mb-0 px-2 px-2 flex text-white">
						<div class="icon ">
							<svg class="fill-current"  width="30" height="30" viewBox="0 0 64 64"><g ><path  d="M50,1H14c-2.209,0-4,1.791-4,4v55c0,0.356,0.189,0.686,0.498,0.865c0.308,0.179,0.688,0.181,0.998,0.003 L32,49.152l20.504,11.716C52.657,60.956,52.829,61,53,61c0.174,0,0.347-0.045,0.502-0.135C53.811,60.686,54,60.356,54,60V5 C54,2.791,52.209,1,50,1z"></path></g></svg>
						</div>
						<div class="icon flex-1 ml-2">
							<h3>Custom Domain</h3>
							<p>Memilih domain atau sub domain kamu sendiri, contoh : wayan-ayu.com atau wayan-inmotioon.com</p>
						</div>
					</div>
					<div class="feature-content w-full md:w-full xl:w-1/3 mb-0 md:mb-0 xl:mb-0 px-2 px-2 flex text-white">
						<div class="icon ">
							<svg class="fill-current"  width="30" height="30" viewBox="0 0 64 64"><g ><path  d="M50,1H14c-2.209,0-4,1.791-4,4v55c0,0.356,0.189,0.686,0.498,0.865c0.308,0.179,0.688,0.181,0.998,0.003 L32,49.152l20.504,11.716C52.657,60.956,52.829,61,53,61c0.174,0,0.347-0.045,0.502-0.135C53.811,60.686,54,60.356,54,60V5 C54,2.791,52.209,1,50,1z"></path></g></svg>
						</div>
						<div class="icon flex-1 ml-2">
							<h3>Bagikan Tanpa Batas</h3>
							<p>Membagikan undangan kamu tanpa Batasan jumlah. Bebas sebarkan link sebanyak-banyaknya.</p>
						</div>
					</div>
				</div>
			</div>
			<div class="h-12 bg-gray-200"></div>
		</section>
		<section id="price" class="min-h-screen bg-gray-100 price">
			<div class="pad w-full h-16 bg-gray-100"></div>
			<div class="content flex-1 bg-gray-100 flex flex-col ">
				<div class="content-title flex justify-between mt-0 md:mt-10 px-12 xl:mt-10">
					<div class="title-text text-red-500 text-4xl">Harga Paket</div>
					<div class="title-line ml-10 flex-1 border-b  border-red-300"></div>
				</div>
				<div class="price-content py-10 md:py-10 xl:py-10 flex flex-col md:flex-col xl:flex-row mt-10">
					<div :class="section=='price'? 'fade-bot':''" class="prices w-full md:w-full xl:w-1/3 px-8">
						<div class="relative w-full h-86 mb-8 md:mb-8 xl:mb-0">
							<div class="package absolute w-full h-86 shadow-lg flex flex-col justify-between bg-white">
								<div class="header-package text-xl font-bold text-red-500 flex h-16 bg-white">
									<span class="block m-auto ">SILVER</span>
								</div>
								<ul class="mt-5 text-sm flex-1 px-4 py-2 font-semibold text-red-400">
									<li class="mb-2">Subdomain URL (inmotioon.com/rumi-juli)</li>
									<li class="mb-2">Amazing design sesuai tema</li>
									<li class="mb-2">Informasi Acara</li>
									<li class="mb-2">Google Maps</li>
									<li class="mb-2">Photo gallery</li>
									<li class="mb-2">Daftar Undangan dan bisa diexport</li>
									<li class="mb-2">Website yang responsive</li>
									<li class="mb-2">Fast Loading (cepat dan ringan)</li>
								</ul>
								<a class="mb-5 mx-auto hover:bg-white hover:text-red-500 w-2/3 h-10 text-center text-white font-bold rounded-full px-2 py-2 bg-red-500 border border-red-500" href="">Rp. 500,000</a>
							</div>
							<div class="shade absolute h-10 bg-white shadow-xl"></div>
						</div>
						
					</div>
					<div :class="section=='price'? 'fade-bot':''" class="prices w-full md:w-full xl:w-1/3 px-8">
						<div class="relative w-full h-86 mb-8 md:mb-8 xl:mb-0">
							<div class="package absolute w-full h-86 shadow-xl flex flex-col justify-between bg-white">
								<div class="header-package text-xl font-bold text-red-500 flex h-16 bg-white">
									<span class="block m-auto">GOLD</span>
								</div>
								<ul class="mt-5 text-sm flex-1 px-4 py-2 font-semibold text-red-400">
									<li class="mb-2">Custom domain URL (namapengantin.com)</li>
									<li class="mb-2">Amazing design sesuai tema</li>
									<li class="mb-2">Informasi Acara</li>
									<li class="mb-2">Google Maps</li>
									<li class="mb-2">Photo Gallery</li>
									<li class="mb-2">Simple auto responder</li>
									<li class="mb-2">Daftar undangan dan bisa diexport</li>
									<li class="mb-2">Website yang responsive</li>
									<li class="mb-2">Fast loading (sepat dang ringan)</li>
								</ul>
								<a class="mb-5 mx-auto hover:bg-white hover:text-red-500 w-2/3 h-10 text-center text-white font-bold rounded-full px-2 py-2 bg-red-500 border border-red-500" href="">Rp. 1,000,000</a>
							</div>
							<div class="shade absolute h-10 bg-white shadow-xl"></div>
						</div>
					</div>
					<div :class="section=='price'? 'fade-bot':''" class="prices w-full md:w-full xl:w-1/3 px-8">
						<div class="relative w-full h-86 mb-8 md:mb-8 xl:mb-0">
							<div class="package absolute w-full h-86 shadow-xl flex flex-col justify-between bg-white">
								<div class="header-package text-xl font-bold text-red-500 flex h-16 bg-white-400">
									<span class="block m-auto">PLATINUM</span>
								</div>
								<ul class="mt-5 text-sm flex-1 px-4 py-2 font-semibold text-red-400">
									<li class="mb-2">Custom domain URL (namapengantin.com)</li>
									<li class="mb-2">Custom design</li>
									<li class="mb-2">Custom feature</li>
									<li class="mb-2">Informasi Acara</li>
									<li class="mb-2">Google Maps</li>
									<li class="mb-2">Photo Gallery</li>
									<li class="mb-2">Simple auto responder</li>
									<li class="mb-2">Daftar undangan dan bisa diexport</li>
									<li class="mb-2">Website yang responsive</li>
									<li class="mb-2">Fast loading (sepat dang ringan)</li>
								</ul>
								<a class="mb-5 mx-auto hover:bg-white hover:text-red-500 w-2/3 h-10 text-center text-white font-bold rounded-full px-2 py-2 bg-red-500 border border-red-500" href="">Rp. 1,500,000</a>
							</div>
							<div class="shade absolute h-10 bg-white shadow-xl"></div>
						</div>
					</div>
				</div>
			</div>
		</section>
		<section id="theme" class="min-h-screen bg-gray-300 flex flex-col theme">
			<div class="pad w-full h-16"></div>
			<div class="content flex flex-1 flex-col">
				<span class="block mx-auto font-sans font-light text-2xl text-gray-600">Oops Theme is under construction..., <span class="font-bold">Play game instead</span></span>
				<iframe class="w-screen h-screen mt-2" src="http://koyoroyo.com/game/"></iframe>
			</div>
		</section>
		<section id="contact" class=" min-h-screen bg-white contact">
			<div class="pad w-full h-16"></div>
			<div class="content flex flex-col px-12">
				<div class="content-title flex justify-between mt-0 md:mt-10 xl:mt-10">
					<div class="title-text text-red-500 text-4xl">Hubungi Kami</div>
					<div class="title-line ml-10 flex-1 border-b  border-red-300"></div>
				</div>
				<div class="contacts-content flex flex-col md:flex-col xl:flex-row mt-10 md:mt-15 xl:mt-20">
					<div class="contact mb-4 md:mb-4 xl:mb-0 w-full md:w-full xl:w-1/4 px-0 md:px-5 xl:px-10">
						<a :class="section=='contact'? 'fadein':''" href="#" class="social-media w-full h-48 bg-red-400 rounded text-white flex">
							<svg class="fill-current m-auto social-icon" width="150" height="150" viewBox="0 0 64 64"><g ><path d="M61,9H3c-1.105,0-2,0.895-2,2v42c0,1.105,0.895,2,2,2h58c1.105,0,2-0.895,2-2V11C63,9.895,62.105,9,61,9z M57.562,15.827l-25,17C32.393,32.942,32.196,33,32,33s-0.393-0.058-0.563-0.173l-25-17c-0.456-0.311-0.575-0.933-0.265-1.39 c0.311-0.455,0.932-0.575,1.39-0.265L32,30.791l24.437-16.618c0.456-0.311,1.079-0.19,1.39,0.265 C58.138,14.895,58.019,15.517,57.562,15.827z"></path></g></svg>
						</a>
					</div>
					<div class="contact mb-4 md:mb-4 xl:mb-0 w-full md:w-full xl:w-1/4 px-0 md:px-5 xl:px-10">
						<a  :class="section=='contact'? 'fadein':''" href="#" class="social-media w-full h-48 bg-red-400 rounded text-white flex">
							<svg class="fill-current m-auto social-icon"  width="115" height="115" viewBox="0 0 438.536 438.536"><g ><path d="M414.41 24.123C398.333 8.042 378.963 0 356.315 0H82.228C59.58 0 40.21 8.042 24.126 24.123 8.045 40.207.003 59.576.003 82.225v274.084c0 22.647 8.042 42.018 24.123 58.102 16.084 16.084 35.454 24.126 58.102 24.126h274.084c22.648 0 42.018-8.042 58.095-24.126 16.084-16.084 24.126-35.454 24.126-58.102V82.225c-.001-22.649-8.043-42.021-24.123-58.102zm-41.255 201.425h-49.963V406.84H248.39V225.548h-37.4V163.02h37.401v-37.402c0-26.838 6.283-47.107 18.843-60.813 12.559-13.706 33.304-20.555 62.242-20.555h49.963v62.526h-31.401c-10.663 0-17.467 1.853-20.417 5.568-2.949 3.711-4.428 10.23-4.428 19.558v31.119h56.534l-6.572 62.527z"></path></g></svg>
						</a>
					</div>
					<div class="contact mb-4 md:mb-4 xl:mb-0 w-full md:w-full xl:w-1/4 px-0 md:px-5 xl:px-10">
						<a :class="section=='contact'? 'fadein':''" href="https://www.instagram.com/undangandigital.bali/" target="_blank" class="social-media w-full h-48 bg-red-400 rounded text-white flex">
							<svg class="fill-current m-auto social-icon"  width="115" height="115" viewBox="0 0 438.536 438.536"><g ><path d="M421.981 16.562C410.941 5.519 397.711 0 382.298 0H56.248C40.83 0 27.604 5.521 16.561 16.562 5.52 27.6.001 40.828.001 56.243V382.29c0 15.413 5.518 28.644 16.56 39.683 11.043 11.04 24.272 16.563 39.687 16.563h326.046c15.41 0 28.644-5.523 39.684-16.563 11.043-11.039 16.557-24.27 16.557-39.683V56.243c-.001-15.418-5.514-28.639-16.554-39.681zM157.462 158.025c17.224-16.652 37.924-24.982 62.097-24.982 24.36 0 45.153 8.33 62.381 24.982 17.228 16.655 25.837 36.785 25.837 60.386 0 23.598-8.609 43.729-25.837 60.379-17.228 16.659-38.014 24.988-62.381 24.988-24.172 0-44.87-8.336-62.097-24.988-17.228-16.652-25.841-36.781-25.841-60.379 0-23.601 8.613-43.73 25.841-60.386zm231.403 212.564c0 4.945-1.718 9.083-5.141 12.416-3.433 3.33-7.519 4.996-12.282 4.996h-305.2c-4.948 0-9.091-1.666-12.419-4.996-3.333-3.326-4.998-7.471-4.998-12.416V185.575H89.08c-3.805 11.993-5.708 24.462-5.708 37.402 0 36.553 13.322 67.715 39.969 93.511 26.65 25.786 58.721 38.685 96.217 38.685 24.744 0 47.583-5.903 68.527-17.703 20.937-11.807 37.486-27.839 49.676-48.112 12.183-20.272 18.274-42.4 18.274-66.38 0-12.94-1.91-25.406-5.715-37.402h38.547V370.59h-.002zm0-254.963c0 5.52-1.903 10.184-5.716 13.99-3.805 3.809-8.466 5.711-13.989 5.711h-49.676c-5.517 0-10.185-1.903-13.99-5.711-3.806-3.806-5.708-8.47-5.708-13.99V68.522c0-5.33 1.902-9.945 5.708-13.848 3.806-3.901 8.474-5.854 13.99-5.854h49.676c5.523 0 10.185 1.952 13.989 5.854 3.812 3.903 5.716 8.518 5.716 13.848v47.104z"></path></g></svg>
						</a>
					</div>
					<div class="contact mb-4 md:mb-4 xl:mb-0 w-full md:w-full xl:w-1/4 px-0 md:px-5 xl:px-10">
						<a :class="section=='contact'? 'fadein':''" href="#" class="social-media w-full h-48 bg-red-400 rounded text-white flex">
							<svg class="fill-current m-auto social-icon" width="115" height="115" viewBox="0 0 16 16"><g ><path  d="M13.641 2.325A7.869 7.869 0 0 0 8.032 0C3.663 0 .107 3.556.107 7.928c0 1.397.366 2.763 1.059 3.963L.041 16l4.203-1.103a7.929 7.929 0 0 0 3.787.966h.003c4.369 0 7.928-3.556 7.928-7.928a7.887 7.887 0 0 0-2.322-5.609zm-5.607 12.2a6.583 6.583 0 0 1-3.356-.919l-.241-.144-2.494.653.666-2.431-.156-.25a6.537 6.537 0 0 1-1.009-3.506 6.599 6.599 0 0 1 6.594-6.591c1.759 0 3.416.688 4.659 1.931a6.554 6.554 0 0 1 1.928 4.662c-.003 3.637-2.959 6.594-6.591 6.594zm3.613-4.937c-.197-.1-1.172-.578-1.353-.644s-.313-.1-.447.1c-.131.197-.512.644-.628.778-.116.131-.231.15-.428.05s-.838-.309-1.594-.984c-.588-.525-.987-1.175-1.103-1.372s-.013-.306.088-.403c.091-.088.197-.231.297-.347s.131-.197.197-.331c.066-.131.034-.247-.016-.347s-.447-1.075-.609-1.472c-.159-.388-.325-.334-.447-.341-.116-.006-.247-.006-.378-.006s-.347.05-.528.247c-.181.197-.694.678-.694 1.653s.709 1.916.809 2.05c.1.131 1.397 2.134 3.384 2.991.472.203.841.325 1.128.419.475.15.906.128 1.247.078.381-.056 1.172-.478 1.338-.941s.166-.859.116-.941c-.047-.088-.178-.137-.378-.238z"></path></g></svg>
						</a>
					</div>
				</div>
				<a class="block hover:bg-red-400 hover:border-transparent hover:text-white rounded-full px-4 py-2 text-red-500 bg-white border border-red-500 font-semibold self-center mt-16 text-sm md:text-base xl:text-base" href="#testimoni">Lihat Testimoni Pelanggan Kami</a>
			</div>
		</section>
		<section id="testimoni" class="min-h-screen bg-gray-100 testimoni">
			<div class="pad w-full h-16"></div>
			<div class="content flex flex-col px-12 py-10 ">
				<div class="content-title flex justify-between mt-0 mt-0 md:mt-10 xl:mt-10">
					<div class="title-text text-red-500 text-4xl">Testimoni</div>
					<div class="title-line ml-10 flex-1 border-b  border-red-300"></div>
				</div>
				<div class="testimoni-content mt-10 md:mt-15 xl:mt-20">
					<swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
						<!-- slides -->
						<swiper-slide><img src="./assets/img/testimoni1.jpg"></swiper-slide>
						<swiper-slide><img src="./assets/img/testimoni1.jpg"></swiper-slide>
						<swiper-slide><img src="./assets/img/testimoni1.jpg"></swiper-slide>
						<swiper-slide><img src="./assets/img/testimoni1.jpg"></swiper-slide>
						<swiper-slide><img src="./assets/img/testimoni1.jpg"></swiper-slide>
						<swiper-slide><img src="./assets/img/testimoni1.jpg"></swiper-slide>
						<swiper-slide><img src="./assets/img/testimoni1.jpg"></swiper-slide>
						<!-- Optional controls -->
						<div class="swiper-pagination"  slot="pagination"></div>
						
					</swiper>
				</div>
			</div>
		</section>
		<footer :class="scroll>40? 'active':''" class="fixed tracking-wider z-20 w-screen md:w-screen xl:w-auto right-0 bottom-0 flex">
			<div class="footer-content text-sm font-sans font-light px-2 py-2 w-full md:w-full xl:w-auto text-center bg-white  md:bg-white xl:bg-white shadow-inner text-gray-700 md:text-gray-700 xl:text-gray-700 xl:rounded-tl xl:rounded-tr">Copyright &copy; Inmotioon 2020</div>
		</footer>
	</div>
</template>
<script>
export default {
	name : 'App',
	data (){
		return {
			scroll : 0,
			section : 'home',
			element : {},
			postitionHome : 0,
			positionAbout : 0,
			positionFeature : 0,
			positionPrice : 0,
			positionTheme : 0,
			positionContact : 0,
			openBar : false,
			swiperOption: {
				effect: 'coverflow',
				grabCursor: true,
				centeredSlides: true,
				slidesPerView: 'auto',
				coverflowEffect: {
					rotate: 50,
					stretch: 0,
					depth: 100,
					modifier: 1,
					slideShadows : true
				},
				pagination: {
					el: '.swiper-pagination'
				}
				
        	},
		}
	},
	computed: {
      swiper() {
        return this.$refs.mySwiper.swiper
      }
    },
	methods : {
		handleScroll(){
			this.scroll = window.scrollY;
			if (this.scroll>=0 && this.scroll < this.positionAbout){
				this.section = 'home';
			}else if (this.scroll>=this.positionAbout && this.scroll < this.positionFeature){
				this.section = 'about';
			}else if (this.scroll>this.positionFeature && this.scroll < this.positionPrice){
				this.section = 'feature';
			}else if (this.scroll>this.positionPrice && this.scroll < this.positionTheme){
				this.section = 'price';
			}else if (this.scroll>this.positionTheme && this.scroll < this.positionContact){
				this.section = 'theme';
			}else if (this.scroll>this.positionContact){
				this.section = 'contact';
			}
		},
		toogleMenu(){
			this.openBar = !this.openBar;
		},

		mapPosition(){
			let elementHome = this.$el.querySelector('.home');
			let elementAbout = this.$el.querySelector('.about');
			let elementFeature = this.$el.querySelector('.feature');
			let elementPrice = this.$el.querySelector('.price');
			let elementTheme = this.$el.querySelector('.theme');
			let elementContact = this.$el.querySelector('.contact');
			
			this.positionAbout = 0 + elementHome.clientHeight - 14-100;
			this.positionFeature = this.positionAbout + elementAbout.clientHeight - 14-100;
			this.positionPrice = this.positionFeature + elementPrice.clientHeight - 14-100;
			this.positionTheme = this.positionPrice + elementTheme.clientHeight - 14-100;
			this.positionContact = this.positionTheme + elementContact.clientHeight - 14-100;
		}
	},
	created(){
		window.addEventListener('scroll',this.handleScroll);
		window.addEventListener('resize',this.mapPosition);
		
	},
	mounted(){
		this.mapPosition();

		this.swiper.slideTo(3, 1000, false)
	},
	destroyed(){
		window.removeEventListener('resize',this.mapPosition);
		window.removeEventListener('scroll',this.handleScroll);
	}
}
</script>


