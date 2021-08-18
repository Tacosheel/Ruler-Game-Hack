let interval = setInterval(() => {
	let arr = document.querySelector('input[name=question]').value.split('-');
	!arr[0]
		? (arr[0] = null)
		: arr[0].includes('/') ? (arr[0] = arr[0].split('/').map((x) => parseInt(x))) : (arr[0] = parseInt(arr[0]));
	arr[1] ? (arr[1] = arr[1].split('/').map((x) => parseInt(x))) : (arr[1] = null);

	let num = arr[1]
		? arr[0] * 16 + arr[1][0] / arr[1][1] * 16
		: Array.isArray(arr[0]) ? arr[0][0] / arr[0][1] * 16 : arr[0] * 16;
	num && document.querySelector('img[name=img' + (num < 10 ? '0' + num : num) + ']').click();
}, 1000);

document.onkeyup = () => clearInterval(interval);
