module.exports = {
	components: { 
		'/api': 'api',
		'/admin': 'admin',
		'/': 'front'
	},
	express: {
		'view engine': 'ejs', 
		'extension': 'html', 
		'view cache': false
	}
};