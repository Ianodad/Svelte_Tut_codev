<script>
	import ChildStyles from './components/ChildStyles.svelte';
	
	import { setContext } from 'svelte'
	import Greet from './components/Greet.svelte'
	import ComponentC from './components/ComponentC.svelte'
	import Popup from './components/Popup.svelte'
	import Outer from './components/Outer.svelte'
	import Button from './components/Button.svelte'

	import Card from './components/Card.svelte'
	import NameList from './components/NameList.svelte'
	import PostList from './components/PostList.svelte';
	import AutoFocus from './components/AutoFocus.svelte'
	
	// Vids 1-8
	// const name = "Ian"
	// const channel = '<b>Master Planner</b>'
	// const success= `<a href="#" onclick="alert('You have been successfully login')">Congrats<a/>`
	// 	const headingId = 'heading'
	// 	const disabled = false
	// 	const status = 'success'
	// 	const isPromoted = false
	// 	const promoted = false
		
	// 	const num = 32
	// 	// List Rendering
	// 	const names =['Bruce', 'Clark', 'Daina']
	// 	const fullNames =[
	// 		{ first: 'Bruce', last: 'Wayne'},
	// 		{ first: 'Clark', last: 'Kent'},
	// 		{ first: 'Princess', last: 'Diana' },
	// 	]
		
	// 	let count = 0
		
	// 	function handleClick(event, stepSize) {
	// 		console.log(event)
	// 		count += stepSize
	// 	}
		
	// 	const formValues = {
	// 		name:'',
	// 		profile:'',
	// 		country:'',
	// 		jobLocation:[],
	// 		remoteWork: false,
	// 		skillsSet:[],
	// 		yearOfExperience:''
			
	// 	}
		
	// 	function submitForm(event){
	// 		console.log(formValues)
	// 	}
		// Reactive Declaration
		
		// let firstName = 'Bruce'
		// let lastName = 'Wayne'
		// $: fullName = `${firstName} ${lastName}`
		
		// let items = [
		// 	{
		// 		id:1,
		// 		title:'TV',
		// 		price: 100
		// 	},
		// 	{
		// 		id:2,
		// 		title:'Phone',
		// 		price: 200
		// 	},
		// 	{
		// 		id:1,
		// 		title:'Laptop',
		// 		price: 300
		// 	},
		// 	{
		// 		id:1,
		// 		title:'Shoes',
		// 		price: 100
		// 	}
			
		// ]
		// $: total = items.reduce((total, curr)=>(total = total +curr.price), 0)
		// let volume = 0
		
		// $: if (volume  < 0){
		// 	alert('cant go lower')
		// 	volume = 0
		// } else if (volume > 20){
		// 	alert('cant go higher')
		// 	volume = 20
		// }
		
		// const chan = 'Codeworld'
		
		// const obj = {
		// 	name:"luke",
		// 	heroName:"king"
		// }
		
		// let showPopup = false
		// function closePopup(event) {
		// 	    showPopup = false
		//     console.log(event.detail)
		//   }
		// setContext('chan-context', chan)
		// function handleGreet(event){
		// 	alert(event.detail)
		// }
		</script>

<main>
	<!-- Vids 1-8 -->
	<!-- <h1>Hello {name} </h1>
		<h2 class={status}>Youtube</h2>
	<div>{@html channel}</div>
	<div>{@html success}</div>
	<h2 id={headingId}>This is a heading</h2> -->
	<!-- <h1 {isPromoted ? 'promoted': disabled}>Movie Title</h1> -->
	<!-- <h1 class:promoted={isPromoted}>Movie Title</h1> -->
	<!-- <h1 class:promoted>Movie Title</h1>
	<button {disabled}>Bind</button> -->

	<!-- VIDS 8-# -->
	<!-- {#if num === 0}
		<h2>The number Is Zero</h2>
	{:else if num < 0}
		<h2>The number is positive</h2>
	{:else if num > 0}
		<h2>The number is negative</h2>
	{:else}
		<h2>The number is not Zero</h2>
	{/if} -->

	<!-- List Rendering -->
	<!-- <h2>LIST OF NAMES</h2>
	{#each names as name, index {name.first}}
		<h2>{index + 1} {name}</h2>
	{/each}
	<h2>FULL NAMES</h2>
	{#each fullNames as name, index {name}}
		<h2>{index + 1} { name.first } { name.last}</h2>
	{/each} -->
	<!-- Binding -->
	<!-- <h2>Hello</h2>
	<button on:click={() => (count  = count + 1)}>Count {count}</button> -->
	<!-- <button on:click={handleClick}>Count {count}</button> -->
	<!-- <button on:click={(event) =>handleClick(event, 5)}>Count {count}</button>
	<button on:click={(event) =>handleClick(event, 10)}>Count {count}</button> -->
	<!-- form handling -->
	<!-- <div>

		<div>
			<pre>{JSON.stringify(formValues, null, 2)}</pre>
		</div>
		<form on:submit|preventDefault ={submitForm}>
			<div>
				<label for="name">Name</label>
				<input type="text" id="name" bind:value={formValues.name}/>
			</div>
			
			<div>
				<label for="profile">profile Summary</label>
				<textarea name="profile" id="profile" cols="30" rows="10" bind:value={formValues.profile}/>			
			</div>
			
			<div>
				<label for="country">Country</label>
				<select name="country" id="country" bind:value={formValues.country}>
					<option value="">Select a country</option>
					<option value="india">India</option>
					<option value="vietnam">Vietnam</option>
					<option value="singapore">Singapore</option>
				</select>
				
			</div>
			
			<div>
				<label for="job-location">Job Location</label>
				<select name="job location" id="job-location" bind:value={formValues.jobLocation} multiple>
					<option value="">Select a country</option>
					<option value="india">India</option>
					<option value="vietnam">Vietnam</option>
					<option value="singapore">Singapore</option>
				</select>
				
			</div>
			
			<div>
				<input type="checkbox" id="remoteWork" bind:checked={formValues.remoteWork} multiple>
				<label for="remoteWork">Open to remote work?</label>
			</div>
			
			<div>
				<label for="">Skill Set</label>
				<input type="checkbox" id="html" value="html" bind:group={formValues.skillsSet}>
				<label for="html">HTML</label>
				<input type="checkbox" id="css" value="css" bind:group={formValues.skillsSet}>
				<label for="css">CSS</label>
				<input type="checkbox" id="javascript" value="javascript" bind:group={formValues.skillsSet}>
				<label for="checkbox">Javascript</label>
			</div>
			
			<div>
				<label for="">Year Of Experience</label>
				<input type="radio" id="0-2" value="0-2" bind:group={formValues.yearOfExperience}/>
				<label for="0-2">0-2</label>
				<input type="radio" id="3-5" value="3-5" bind:group={formValues.yearOfExperience}/>
				<label for="3-5">3-5</label>
				<input type="radio" id="6-10" value="6-10" bind:group={formValues.yearOfExperience}/>
				<label for="6-10">6-10</label>
			</div>
			
			<div>
				<button type="submit">Submit</button>
			</div>
		</form>
	</div> -->
	<!-- REAXTOVE DEVLARATIONS -->
	<!-- <div>
		<p>{firstName}</p>
		<p>{lastName}</p>
		<p>{fullName}</p>
	</div>
	<div>
		<p>Total {total}</p>
	</div>
	<h2>Current Volume {volume}</h2>
	<button on:click={()=> (volume += 2)}>Increment volume</button>
	<button on:click={()=> (volume -= 2)}>Decrease volume</button> -->

	<!-- COMPONENT  -->

	<!-- <Greet name="Ian" heroName="point 1"/>
	<Greet name="John" heroName="point 2"/>
	<Greet name="Jack" heroName="point 3"/>
	<Greet name={name} heroName={chan}/>
	<Greet {...obj}/>

	<h2>ComponentC</h2>
	<ComponentC/>
	{#if !showPopup}
		<button on:click={()=> showPopup = true}>Show Popup</button>
	{/if}
	{#if showPopup}
		<Popup on:close={closePopup}/>
	{/if} -->

	<!-- <Outer on:greet={handleGreet}/>
	<Button on:click={()=> alert('clicked')}></Button> -->
	<!-- <Card>Card content</Card>
	<Card><h2>Card content</h2></Card>

	<Card><img src="https://picsum.photos/200" alt/></Card> -->

	<!-- <Card content='Card content 1' />
	<Card content='Card content 2' /> -->

	<!-- <Card>
		<div slot="header">
			<h2>Header</h2>
		</div>
		<div slot='content'>
			<img src='https://picsum.photos/200' alt/>
		</div>
		<div slot='footer'>
			<button>View Details</button>
		</div>
	</Card> -->

	<!-- <NameList>
		<h3 slot='hero' let:firstName let:lastName>
			{firstName} {lastName}
		</h3>
	</NameList>
	<NameList>
		<h3 slot='hero' let:firstName let:lastName>
			{firstName}, {lastName}
		</h3>
	</NameList>
	<NameList>
		<h3 slot='hero' let:firstName let:lastName>
			{firstName}
		</h3>
	</NameList> -->
	<!-- <PostList/> -->
	<AutoFocus/>
	<!-- <h4>App components text</h4> -->
	<!-- <ChildStyles/> -->
</main>
	<style>

	:global(h3){
		color: blue;
	}
	
	h4 { 
		color:orange;
	}

	input + label {
		display: inline-flex;
	}

	main {
		/* text-align: center; */
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		}
		
	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
	.promoted {
		text-decoration: wavy;
		text-transform: uppercase;
	}
	.danger {
		color: red;
	}

	.success {
		color: olive;
	}

	#heading {
		color: #ff3e00;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>