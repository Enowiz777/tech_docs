# React

# React Hook

## 1. Form

You can use Register Function to create a form.

*What are your goals?*
1. Less code.
2. Better validation.
3. Better errors (set, clear and display)
4. Have control over input
5. Don't deal with events.

*How do you install react-hook-form?*
- It is already installed.

*What are the rule of thumb*
1. Everything comes from useForm.
2. You use register function that connects input to the state.

*What happen if you print register function?*
{...register} will create all other things necessary such as name, onChange, and others.

- With one code <input {{...register("email")}>, it is same as
	1. Creating state
	2. Register eventlister
	3. Put eventListener value inside the input tag.

### 1.1 Watch function
