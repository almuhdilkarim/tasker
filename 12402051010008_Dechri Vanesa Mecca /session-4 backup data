/*M!999999\- enable the sandbox mode */ 
-- MariaDB dump 10.19  Distrib 10.11.13-MariaDB, for debian-linux-gnu (x86_64)
--
-- Host: localhost    Database: vanelibrary
-- ------------------------------------------------------
-- Server version	10.11.13-MariaDB-0ubuntu0.24.04.1

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `list_musik_harian`
--

DROP TABLE IF EXISTS `list_musik_harian`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8mb4 */;
CREATE TABLE `list_musik_harian` (
  `id_musik` int(11) NOT NULL AUTO_INCREMENT,
  `judul_lagu` varchar(100) NOT NULL,
  `penyanyi` varchar(100) DEFAULT NULL,
  `genre` varchar(50) DEFAULT NULL,
  `waktu_dengar` datetime DEFAULT NULL,
  `durasi_dengar` int(11) DEFAULT NULL,
  `platform` varchar(50) DEFAULT NULL,
  `rating` int(11) DEFAULT NULL CHECK (`rating` between 1 and 5),
  `catatan` text DEFAULT NULL,
  PRIMARY KEY (`id_musik`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `list_musik_harian`
--

LOCK TABLES `list_musik_harian` WRITE;
/*!40000 ALTER TABLE `list_musik_harian` DISABLE KEYS */;
INSERT INTO `list_musik_harian` VALUES
(1,'Story of My Life','One Direction','Folk Pop','2025-10-11 10:00:00',240,'Spotify',5,'Lagu favorit.'),
(2,'Bad Idea Right','Olivia Rodrigo','Pop Rock','2025-10-11 10:04:00',180,'Spotify',5,'Lagu favorit.'),
(3,'Incomplete','Backstreet Boys','Pop Rock','2025-10-11 10:10:00',240,'Spotify',5,'Lagu favorit.'),
(4,'Supermassive Black Hole','Muse','Rock','2025-10-11 10:14:00',180,'Spotify',5,'Lagu favorit.'),
(5,'Human Nature','Michael Jackson','R&B','2025-10-11 10:20:00',240,'Spotify',5,'Lagu favorit.');
/*!40000 ALTER TABLE `list_musik_harian` ENABLE KEYS */;
UNLOCK TABLES;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2025-10-19 20:55:29
