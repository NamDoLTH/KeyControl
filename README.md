package blockbattle

case class KeyControl(left: String, right: String, up: String, down: String){
  def direction(key: String): (Int, Int) = key match{
    case `left` => (-1,0)
    case `right` => (1,0)
    case `up` => (0,-1)
    case `down` => (0,1)
    case _ => (0,0)
  }
  def has(key: String): Boolean = key match {
    case `left` => true
    case `right` => true
    case `up` => true
    case `down` => true
    case _ => false
  }
}
