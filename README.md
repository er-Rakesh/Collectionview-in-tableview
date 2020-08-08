# Collectionview-in-tableview


func collectionView(_ collectionView: UICollectionView, cellForItemAt indexPath: IndexPath) -> UICollectionViewCell {

    if let cell: CollectionViewCell = collectionView.dequeueReusableCell(withReuseIdentifier: "CollectionViewCell", for: indexPath) as? CollectionViewCell
   // if let cell: UICollectionView = collectionView.dequeueReusableCell(withReuseIdentifier: "CollectionViewCell", for: indexPath) as! CollectionViewCell
                        
{
    let randomNumber = Int(arc4random_uniform(UInt32(UInt64(imageArray.count))))
cell.imageView.image = UIImage(named: imageArray[randomNumber])
return cell
}
    
return UICollectionViewCell()
}
    
    
func collectionView(_ collectionView: UICollectionView, layout collectionViewLayout: UICollectionViewLayout, sizeForItemAt indexPath: IndexPath) -> CGSize{
//let size = CGSize(width: 120, height: 120)
//return size
    return CGSize(width: self.collectionView.frame.size.width/2-20, height: 120)

}
    
