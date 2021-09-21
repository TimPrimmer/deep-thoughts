# MERN stack project


query {
  # get all users
  users {
    username
    email
  }

  # get a single user by username (use a username from your database)
  user(username: "Brannon.Jacobs") {
    username
    email
    friendCount
    thoughts {
      thoughtText
    }
    friends {
      username
    }
  }

  # query all thoughts
  thoughts {
    _id
    username
    thoughtText
    reactions {
      _id
      createdAt
      username
      reactionBody
    }
  }

  # query a single thought (use an _id from a thought in your database)
  thought(_id: "614a56f8090e512bb41d73f3") {
    _id
    username
    thoughtText
    createdAt
    reactions {
      username
      reactionBody
    }
  }
}