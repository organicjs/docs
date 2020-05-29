module.exports = {
    'get /tasks': 'TaskController.findAll',
    'get /tasks/:id': 'TaskController.findOne',
    'post /tasks': 'TaskController.createNew'
}