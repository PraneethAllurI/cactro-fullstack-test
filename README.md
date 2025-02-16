apiEndPoints = {
    http://localhost:4000/api/polls/${poll._id},
    http://localhost:4000/api/polls,
    http://localhost:4000/api/polls/${poll._id}/vote
}


dbSchema :  {
const mongoose = require('mongoose');

const pollSchema = new mongoose.Schema({
  question: String,
  options: [{
    option: String,
    votes: { type: Number, default: 0 }
  }]
});
const Poll = mongoose.model('Poll', pollSchema);

module.exports = Poll;
}

